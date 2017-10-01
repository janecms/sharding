## 并发基础
-什么是线程?
	–线程是进程内的执行单元

### 线程的基本操作

-	终止线程
	– Thread.stop()不推荐使用。它会释放所有monitor
-	中断线程
```
publicvoidThread.interrupt()//中断线程
publicbooleanThread.isInterrupted()//判断是否被中断
publicstaticbooleanThread.interrupted()//判断是否被中断，并清除当前中断状态
```
	挂起（suspend）和继续执行（resume）线程
	suspend()不会释放锁
	如果加锁发生在resume()之前，则死锁发生???
	等待线程结束（join）和谦让(yeild)

```
publicfinalvoidjoin()throwsInterruptedException
publicfinalsynchronizedvoidjoin(longmillis)throwsInterruptedException
```
```
join的本质
while(isAlive()){
	wait(0);
}
```
守护线程
	-在后台默默地完成一些系统性的服务，比如垃圾回收线程、JIT线程就可以理解为守护线程
	-当一个Java应用内，只有守护线程时，Java虚拟机就会自然退出
-线程优先级	
```
publicfinalstaticintMIN_PRIORITY=1;
publicfinalstaticintNORM_PRIORITY=5;
publicfinalstaticintMAX_PRIORITY=10;
```

**线程同步操作**
-synchronized
	–指定加锁对象：对给定对象加锁，进入同步代码前要获得给定对象的锁。
	–直接作用于实例方法：相当于对当前实例加锁，进入同步代码前要获得当前实例的锁。
	–直接作用于静态方法：相当于对当前类加锁，进入同步代码前要获得当前类的锁。
-Object.wait()Obejct.notify()

---
## 内存模型&线程安全
- 原子性
	是指一个操作是不可中断的。即使是在多个线程一起执行的时候，一个操作一旦开始，就不会被其它线程干扰。
- 有序性
	在并发时，程序的执行可能就会出现乱序
- 可见性	
	指当一个线程修改了某一个共享变量的值，其他线程是否能够立即知道这个修改
	-译器优化
	–硬件优化（如写吸收，批操作）
	[聊聊并发（一）——深入分析Volatile的实现原理](http://www.infoq.com/cn/articles/ftf-java-volatile)

**Happen-Before规则**
-程序顺序原则：一个线程内保证语义的串行性
-volatile规则：volatile变量的写，先发生于读，这保证了volatile变量的可见性
-锁规则：解锁（unlock）必然发生在随后的加锁（lock）前
-传递性：A先于B，B先于C，那么A必然先于C
-线程的start()方法先于它的每一个动作
-线程的所有操作先于线程的终结（Thread.join()）
-线程的中断（interrupt()）先于被中断线程的代码
-对象的构造函数执行结束先于finalize()方法

**无锁类的原理**
- 1.1.CAS
	CAS算法的过程是这样：它包含3个参数CAS(V,E,N)。V表示要更新的变量，E表示预期值，N表示新值。仅当V
	值等于E值时，才会将V的值设为N，如果V值和E值不同，则说明已经有其他线程做了更新，则当前线程什么
	都不做。最后，CAS返回当前V的真实值。CAS操作是抱着乐观的态度进行的，它总是认为自己可以成功完成
	操作。当多个线程同时使用CAS操作一个变量时，只有一个会胜出，并成功更新，其余均会失败。失败的线程
	不会被挂起，仅是被告知失败，并且允许再次尝试，当然也允许失败的线程放弃操作。基于这样的原理，CAS
	操作即时没有锁，也可以发现其他线程对当前线程的干扰，并进行恰当的处
	
	-AtomicStampedReference解决了ABA问题

**各种同步控制工具**
- 1.1.ReentrantLock
	-1.1.1.可重入
	-1.1.2.可中断lockInterruptibly()
	-1.1.3.可限时	
		超时不能获得锁，就返回false，不会永久等待构成死锁
	1.1.4.公平锁
	```
	先来先得
		publicReentrantLock(booleanfair)
		publicstaticReentrantLockfairLock=newReentrantLock(true);
	```
- 1.2.Condition	
```
voidawait()throwsInterruptedException;
voidawaitUninterruptibly();
longawaitNanos(longnanosTimeout)throwsInterruptedException;
booleanawait(longtime,TimeUnitunit)throwsInterruptedException;
booleanawaitUntil(Datedeadline)throwsInterruptedException;
voidsignal();
voidsignalAll();
```
	类似于Object.wait()和Object.notify();与ReentrantLock结合使用
	await()方法会使当前线程等待，同时释放当前锁，当其他线程中使用signal()时或者signalAll()方法时，
	线程会重新获得锁并继续执行。或者当线程被中断时，也能跳出等待。这和Object.wait()方法很相似。
	awaitUninterruptibly()方法与await()方法基本相同，但是它并不会再等待过程中响应中断。
	singal()方法用于唤醒一个在等待中的线程。相对的singalAll()方法会唤醒所有在等待中的线程。这和Obej
	ct.notify()方法很类似。

- 1.3.Semaphore
	共享锁;运行多个线程同时临界区

-	1.4.ReadWriteLock
		-ReadWriteLock是JDK5中提供的读写分离锁
		-读-读不互斥：读读之间不阻塞。
		-读-写互斥：读阻塞写，写也会阻塞读。
		-写-写互斥：写写阻塞。

- 1.5.CountDownLatch:倒数计时器
- 1.6.CyclicBarrier:循环栅栏计数器可以反复使用。
- 1.7.LockSupport:提供线程阻塞原语
```
LockSupport.park();
LockSupport.unpark(t1);
```
**与suspend()比较,不容易引起线程冻结**
**
能够响应中断，但不抛出异常。
中断响应的结果是，park()函数的返回，可以从Thread.interrupted()得到中断标志
**

-----
### 1.3.1.线程池的种类
-newFixedThreadPool
-newSingleThreadExecutor
-newCachedThreadPool
-newScheduledThreadPool

### 2.扩展和增强线程池
-	2.1.回调接口
		-beforeExecute
		-afterExecute
		-terminated
-	2.2.拒绝策略
-	2.3.自定义ThreadFactory		
## 4.ForkJoin

- 4.2.1.RecursiveAction
	无返回值
- 4.2.2.RecursiveTask
	有返回值

	**工作窃取**

---
Future模式	


---
## NIO

–NIO是基于块（Block）的，它以块为基本单位处理数据
–为所有的原始类型提供（Buffer）缓存支持
–增加通道（Channel）对象，作为新的原始I/O抽象
–支持锁和内存映射文件的文件访问接口
–提供了基于Selector的异步网络I/O	

Buffer中有3个重要的参数：位置（position）、容量（capactiy）和上限（limit）

```
publicfinalBufferrewind()
	将position置零，并清除标志位（mark）
publicfinalBufferclear()
		将position置零，同时将limit设置为capacity的大小，并清除了标志mark
publicfinalBufferflip()
	先将limit设置到position所在位置，然后将position置零，并清除标志位mark;通常在读写转换时使用
```	

AIO
-读完了再通知我
-不会加快IO，只是在读完后进行通知
-使用回调函数，进行业务处理	

---

## 锁的优化

### 锁优化的思路和方法

-减少锁持有时间
-减小锁粒度
	-	将大对象，拆成小对象，大大增加并行度，降低锁竞争
	-偏向锁，轻量级锁成功率提高
	-ConcurrentHashMap（若干个SegmentSegment中维护HashEntry）
	-HashMap的同步实现
-锁分离
	-根据功能进行锁分离
	-ReadWriteLock
	-读写分离思想可以延伸，只要操作互不影响，锁就可以分离。LinkedBlockingQueue
-锁粗化
	
	通常情况下，为了保证多线程间的有效并发，会要求每个线程持有锁的时间尽量短，即在使用完
	公共资源后，应该立即释放锁。只有这样，等待在这个锁上的其他线程才能尽早的获得资源执行
	任务。但是，凡事都有一个度，如果对同一个锁不停的进行请求、同步和释放，其本身也会消耗
	系统宝贵的资源，反而不利于性能的优化
	
-锁消除
	在即时编译器时，如果发现不可能被共享的对象，则可以消除这些对象的锁操作（-XX:+EliminateLocks）

###虚拟机内的锁优化

-偏向锁
-轻量级锁
-自旋锁

####对象头Mark

MarkWord，对象头的标记，32位
描述对象的hash、锁信息，垃圾回收标记，年龄
	–指向锁记录的指针
	–指向monitor的指针
	–GC标记
	–偏向锁线程ID	
	
####偏向锁

-大部分情况是没有竞争的，所以可以通过偏向来提高性能
-所谓的偏向，就是偏心，即锁会偏向于当前已经占有锁的线程
-将对象头Mark的标记设置为偏向，并将线程ID写入对象头Mark
-只要没有竞争，获得偏向锁的线程，在将来进入同步块，不需要做同步
-当其他线程请求相同的锁时，偏向模式结束
--XX:+UseBiasedLocking默认启用
-在竞争激烈的场合，偏向锁会增加系统负担

####轻量级锁

- 如果对象没有被锁定
	– 将对象头的Mark指针保存到锁对象中
	– 将对象头设置为指向锁的指针（在线程栈空间中）
-如果轻量级锁失败，表示存在竞争，升级为重量级锁（常规锁）
-在没有锁竞争的前提下，减少传统锁使用OS互斥量产生的性能损耗
-在竞争激烈时，轻量级锁会多做很多额外操作，导致性能下降	

####自旋锁
当竞争存在时，如果线程可以很快获得锁，那么可以不在OS层挂起线程，让线程做几个空操作（自旋）
-JDK1.6中-XX:+UseSpinning开启
-JDK1.7中，去掉此参数，改为内置实现
-如果同步块很长，自旋失败，会降低系统性能
-如果同步块很短，自旋成功，节省线程挂起切换时间，提升系统性

**内置于JVM中的获取锁的优化方法和获取锁的步骤**

	–偏向锁可用会先尝试偏向锁
	–轻量级锁可用会先尝试轻量级锁
	–以上都失败，尝试自旋锁
	–再失败，尝试普通锁，使用OS互斥量在操作系统层挂起
	
### JDK8对并发的新支持
-LongAdder
-CompletableFuture
	- 完成后得到通知
	- 异步执行
	- 流式调用
-StampedLock
–读写锁的改进
-读不阻塞写