# Hystrix高可用技术框架
- Hystrix 提升分布式系统的可用性和稳定性。netflix开源
- Hystrix 设计原则
	- 对依赖服务调用出现的延迟和失败，进行控制和保护，阻止依赖服务耗尽资源
	- 阻止某一个故障蔓延。采用资源隔离技术(bulkhead舱壁隔离），swimlane(泳道技术),circuit breaker(短路技术)
	- 提供fail-fast(快速失败）和快速恢复的支持，避免请求排队和积压；
	- 提供fallback优雅降级的支持
	- 近实时的监控，报警和运维操作(配置热修改，提高恢复和故障处理的速度)
	
- 实现
	- HystrixCommand 或HystrixObservableCommand封装外部依赖的访问请求，这个请求一般运行在独立线程中
	- 对于超出阀值的服务调用，直接进行超时，不允许耗费过长时间，超时时间默认为99.5%的访问时间
	- 为没一个依赖服务维护一个独立的线程池，或是semaphore,当线程已满，直接拒绝对这个服务的调用
	- 成功次数，失败次数，拒绝次数，超时次数进行统计
	- 依赖服务调用失败次数超过了一定阀值，自动熔断，一定时间内调用直接降级，一段时间内在自动尝试恢复
	- 对属性和配置的修改，近实时修改。

	- 命令
		-	HystrixCommand：是用来获取一条数据的
		-	HystrixObservableCommand：是设计用来获取多条数据

- 样例		
```
public class CommandHelloWorld extends HystrixCommand<String> {

    private final String name;

    public CommandHelloWorld(String name) {
        super(HystrixCommandGroupKey.Factory.asKey("ExampleGroup"));
        this.name = name;
    }

    @Override
    protected String run() {
        return "Hello " + name + "!";
    }

}
```

		
```
public class ObservableCommandHelloWorld extends HystrixObservableCommand<String> {

    private final String name;

    public ObservableCommandHelloWorld(String name) {
        super(HystrixCommandGroupKey.Factory.asKey("ExampleGroup"));
        this.name = name;
    }

    @Override
    protected Observable<String> construct() {
        return Observable.create(new Observable.OnSubscribe<String>() {
            @Override
            public void call(Subscriber<? super String> observer) {
                try {
                    if (!observer.isUnsubscribed()) {
                        observer.onNext("Hello " + name + "!");
                        observer.onNext("Hi " + name + "!");
                        observer.onCompleted();
                    }
                } catch (Exception e) {
                    observer.onError(e);
                }
            }
         } ).subscribeOn(Schedulers.io());
    }
}
```	
	
## command的四种调用方式

- 同步：
	- new CommandHelloWorld("World").execute()
	- new ObservableCommandHelloWorld("World").toBlocking().toFuture().get()

如果你认为observable command只会返回一条数据，那么可以调用上面的模式，去同步执行，返回一条数据

- 异步：
	-	new CommandHelloWorld("World").queue()，
	-	new ObservableCommandHelloWorld("World").toBlocking().toFuture()

对command调用queue()，仅仅将command放入线程池的一个等待队列，就立即返回，拿到一个Future对象，后面可以做一些其他的事情，
然后过一段时间对future调用get()方法获取数据	
	
## hystrix，资源隔离两种技术，
-	线程池的资源隔离，
	
	适合绝大多数的场景，99%的，线程池，对依赖服务的网络请求的调用和访问，timeout这种问题
	*具体操作由Hstrix线程池处理，限流是通过线程池的大小来控制的*
	
-	信号量的资源隔离
	
	*具体操作由服务器自己线程池处理 ，但是通过信号量的容量来进行限流*
	*一般用信号量常见于那种基于纯内存的一些业务逻辑服务，而不涉及到任何网络访问请求*
	适合你的访问不是对外部依赖的访问，而是对内部的一些比较复杂的业务逻辑的访问，
	但是像这种访问，系统内部的代码，其实不涉及任何的网络请求，那么只要做信号量的普通限流就可以了，
	因为不需要去捕获timeout类似的问题，算法+数据结构的效率不是太高，并发量突然太高，
	因为这里稍微耗时一些，导致很多线程卡在这里的话，不太好，所以进行一个基本的资源隔离和访问，
	避免内部复杂的低效率的代码，导致大量的线程被hang住

```
// to use thread isolation
HystrixCommandProperties.Setter()
   .withExecutionIsolationStrategy(ExecutionIsolationStrategy.THREAD)
// to use semaphore isolation
HystrixCommandProperties.Setter()
   .withExecutionIsolationStrategy(ExecutionIsolationStrategy.SEMAPHORE)
```	


netflix有100+的command运行在40+的线程池中，只有少数command是不运行在线程池中的，就是从纯内存中获取一些元数据，
或者是对多个command包装起来的facacde command，是用信号量限流的

## 2、command名称和command组

线程池隔离，依赖服务->接口->线程池，如何来划分

你的每个command，都可以设置一个自己的名称，同时可以设置一个自己的组
```
private static final Setter cachedSetter = 
    Setter.withGroupKey(HystrixCommandGroupKey.Factory.asKey("ExampleGroup"))
        .andCommandKey(HystrixCommandKey.Factory.asKey("HelloWorld"));    

public CommandHelloWorld(String name) {
    super(cachedSetter);
    this.name = name;
}
```
command group，是一个非常重要的概念，默认情况下，因为就是通过command group来定义一个线程池的，
而且还会通过command group来聚合一些监控和报警信息
同一个command group中的请求，都会进入同一个线程池中


## 3、command线程池

threadpool key代表了一个HystrixThreadPool，用来进行统一监控，统计，缓存

默认的threadpool key就是command group名称

每个command都会跟它的threadpool key对应的thread pool绑定在一起

如果不想直接用command group，也可以手动设置thread pool name

public CommandHelloWorld(String name) {
    super(Setter.withGroupKey(HystrixCommandGroupKey.Factory.asKey("ExampleGroup"))
            .andCommandKey(HystrixCommandKey.Factory.asKey("HelloWorld"))
            .andThreadPoolKey(HystrixThreadPoolKey.Factory.asKey("HelloWorldPool")));
    this.name = name;
}

- command threadpool -> command group -> command key
  
- command key，代表了一类command，一般来说，代表了底层的依赖服务的一个接口
  
- command group，代表了某一个底层的依赖服务，合理，一个依赖服务可能会暴露出来多个接口，每个接口就是一个command key
  
- command group，在逻辑上去组织起来一堆command key的调用，统计信息，成功次数，timeout超时次数，失败次数，
	可以看到某一个服务整体的一些访问情况
  
- command group，一般来说，推荐是根据一个服务去划分出一个线程池，command key默认都是属于同一个线程池的
  
-比如说你以一个服务为粒度，估算出来这个服务每秒的所有接口加起来的整体QPS在100左右

你调用那个服务的当前服务，部署了10个服务实例，每个服务实例上，其实用这个command group对应这个服务，给一个线程池，量大概在10个左右，就可以了，
你对整个服务的整体的访问QPS大概在每秒100左右
***
一般来说，command group是用来在逻辑上组合一堆command的。
服务command group内部，包含的对应多个接口的command key，做一些细粒度的资源隔离
***

## 4、coreSize

设置线程池的大小，默认是10

```
HystrixThreadPoolProperties.Setter()
   .withCoreSize(int value)
```
一般来说，用这个默认的10个线程大小就够了

## 5、queueSizeRejectionThreshold

控制queue满后reject的threshold，因为maxQueueSize不允许热修改，因此提供这个参数可以热修改，控制队列的最大大小

HystrixCommand在提交到线程池之前，其实会先进入一个队列中，这个队列满了之后，才会reject

默认值是5

```
HystrixThreadPoolProperties.Setter()
   .withQueueSizeRejectionThreshold(int value)
```

## 6、execution.isolation.semaphore.maxConcurrentRequests

设置使用SEMAPHORE隔离策略的时候，允许访问的最大并发量，超过这个最大并发量，请求直接被reject

这个并发量的设置，跟线程池大小的设置，应该是类似的，但是基于信号量的话，性能会好很多，而且hystrix框架本身的开销会小很多

默认值是10，设置的小一些，否则因为信号量是基于调用线程去执行command的，而且不能从timeout中抽离，
因此一旦设置的太大，而且有延时发生，可能瞬间导致tomcat本身的线程资源本占满.

```
HystrixCommandProperties.Setter()
   .withExecutionIsolationSemaphoreMaxConcurrentRequests(int value)
```