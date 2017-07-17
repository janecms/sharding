## 1.java 中的关键字 final 可以用来修饰什么，分别起什么作用。
	final 表示"不可变",可以用来修饰类，属性，和变量。

-	1)修饰类：表示类不可被继承；常见的如Integer.java,Float.java,String.class。

-	2)修饰类属性:表示不能修改，必须在实例初始化之前进行初始化。一般使用于不变(Immutable)模式中，
	 在并发设计中，不变对象是线程安全的，降低并发编程复杂度。

-	3)修饰局部变量：同样表示变量不允许修改，一般使用在匿名内部类参数;
	但是如果修饰变量为数组或引用类型时，仅仅表示对象引用不可变，但对象值域是仍然可变的。

## 2.请说明 ArrayList，Vector，LinkedList 的存档性能和特性。

- 1) 都是有序集合接口java.util.List的的实现。
- 2）Vector和ArrayList底层实现都是Object[]数组。支持索引随机访问元素。区别是Vector通过将方法声明为synchronized方法，实现线程安全，所以,Vector相对ArrayList,
	性能要差。LinkedList，使用双向链表实现存储，按序号索引数据需要进行前向或后向遍历，
- 3）Vector和ArrayList插入数据时，，可能引起数组容量变化，会引起数据复制。
	通常Vector 默认增长为原来一培，而ArrayList却是原来的一半，所以存放大量数据时，两者较LinkedList性能差，
- 4) 随机访问时，一般使用ArrayList,Vector;存放大容量数据，考虑性能倾向于选择LinkedList.


## 3.String，StringBuffer，StringBuilder 有什么区别。
- 1) String 字符串常量;StringBuffer 字符串变量（线程安全）;StringBuilder 字符串变量（非线程安全）
- 2) StringBuffer在任何时间点，包含一些特定的字符序列，但可以通过某些方法调用来更改序列的长度和内容。
- 3) StringBuilder是1.5新增接口，与StringBuffer一样是AbstractStringBuilder的子类，表示一个可变的字符序列。
	该类提供与StringBuffer兼容的API，但不是线程安全。

## 4.swith 是否能作用在 byte 上，是否能作用在 long 上，是否能作用在 strng 上。
- Java SE 7 规定switch表达式类型必须是char，byte，short，int，Character，Byte，Short，Integer，String或枚举类型;
- Java SE 6 规定switch表达式类型必须是char，byte，short，int，Character，Byte，Short，Integer或枚举类型，否则会发生编译时错误

## 7.float 是多少位的。
- float的范围是由指数的位数来决定的。float的指数位有8位; float的范围为-2^128 ~ +2^128
- float的精度是由尾数的位数来决定的,浮点数在内存中是按科学计数法来存储的，其整数部分始终是一个隐含着的“1”，
	影响精度的一共七位，这意味着最多能有7位有效数字，但绝对能保证的为6位，也即float的精度为6~7位有效数字。
## 8. 设计四个线程，其中两个线程每次对 J 增加 1，另外两个线程每次对 J 减 1，写出程序或者思路。
```
public class T {
    private static final AtomicInteger minuxNextId = new AtomicInteger(0);
    private static final AtomicInteger additionNextId = new AtomicInteger(0);
    static  AtomicLong J=new AtomicLong(0);
   static Random random=  new Random();
    static  class MinusTask  implements  Runnable{
        @Override
        public void run() {
            while(true){
                synchronized (J){
                    minuxNextId.incrementAndGet();
                    J.decrementAndGet();
                    Thread.yield();
                }
            }

        }
    }

    static class AddTask  implements  Runnable{
        @Override
        public void run() {
            while(true){
//                try {
//                    TimeUnit.SECONDS.sleep(random.nextInt(10));
//                } catch (InterruptedException e) {
//                }
                synchronized (J){
                    additionNextId.incrementAndGet();
                    J.incrementAndGet();
                    Thread.yield();
                }
            }
        }
    }

    static class MonitorTask implements  Runnable{
      Random random=  new Random();
        @Override
        public void run() {
            while (true){
                try {
                    TimeUnit.SECONDS.sleep(random.nextInt(10));
                } catch (InterruptedException e) {
                }
                synchronized (J){
                    int a =additionNextId.get();
                    int m = minuxNextId.get();
                    int detal =a-m;
                    if(detal==J.get()){
                        System.out.println("j="+J.get()+",共减了"+m+"次,共加了"+a+"次,detal="+detal);
                    }else{
                        System.err.println("j="+J.get()+",共减了"+m+"次,共加了"+a+"次,detal="+detal);
                    }
                }
            }
        }

    }

    public static void main(String[] args) {
            Runnable addTask = new AddTask();
            Runnable minusTask = new MinusTask();
            new Thread(addTask).start();
            new Thread(addTask).start();
            new Thread(minusTask).start();
            new Thread(minusTask).start();
            new Thread(new MonitorTask()).start();

    }
}
```
- 1)一共启动5个线程，2个加线程,2个减线程，1个监控线程。其中监控线程主要用来检查线程安全性。
- 2)使用Runnable接口，实现对象共享；使用AtomicInteger,AtomicLong自身的线程安全性。
- 3)使用synchronized块，按共享变量J为单位加锁，保证组合变量线程安全性。

## 9.a.hashCode（）有什么作用？与 a.equals（b）有什么关系？
 
- 1)hashCode() 的作用是获取哈希码，也称为散列码；它实际上是返回一个int整数。这个哈希码的作用是确定该对象在散列表(HashMap，Hashtable，HashSet)中的索引位置。
- 2)按场景区分：散列表数据结构中：对象hashCode()相等，不一定相等;两个对象相等，那么它们的hashCode()值一定相同;反之：两者没有一点关系。
- 3）Object.java提供equals方法的默认实现,"比较“p1和p2是否是同一个对象”,一般情况下，要重写方法。
- 4） hashcode方法是native方法，满足规则（对象equals相等，hashCode值一定相同;hashCode值相同,对象不一定相等,但是，为不等对象生成不同的整数结果可能会提高哈希表的性能)

## 10. 写出 hashMap 的数据结构。
![hashmap1](http://wiki.jikexueyuan.com/project/java-collection/images/hashmap1.jpg)

如图,HashMap 底层就是一个数组结构，数组中的每一项是一个链表(Entity),称为“桶”。
特点
- 1)HashMap 是基于哈希表的 Map 接口的非同步实现。此实现提供所有可选的映射操作，并允许使用 null 值和 null 键。
- 2)不保证映射的顺序。
- 3)通过hash值，决定对象在散列表中位置
- 4)HashMap有两个参数影响其性能：初始容量和加载因子。默认初始容量是16，加载因子是0.75。容量是哈希表中桶(Entry数组)的数量，
	初始容量只是哈希表在创建时的容量。加载因子是哈希表在其容量自动增加之前可以达到多满的一种尺度。
	当哈希表中的条目数超出了加载因子与当前容量的乘积时，通过调用 rehash 方法将容量翻倍。
	
## 11. 简述 MVC 设计模式。

	![MVC-Process.svg](https://zh.wikipedia.org/wiki/File:MVC-Process.svg)
	将应用程序划分为三种组件，模型 - 视图 - 控制器（MVC）设计定义它们之间的相互作用。
- 1)模型（Model） 用于封装与应用程序的业务逻辑相关的数据以及对数据的处理方法。“ Model ”有对数据直接访问的权力，例如对数据库的访问。
	“Model”不依赖“View”和“Controller”，也就是说， Model 不关心它会被如何显示或是如何被操作。但是 Model 中数据的变化一般会通过一种刷新机制被公布。
	为了实现这种机制，那些用于监视此 Model 的 View 必须事先在此 Model 上注册，从而，View 可以了解在数据 Model 上发生的改变。
	如(DTO, POCO, POJO 等,Repository Pattern ,ORM)
- 2)视图（View）能够实现数据有目的的显示（理论上，这不是必需的）。在 View 中一般没有程序上的逻辑。为了实现 View 上的刷新功能，如JSP
	View 需要访问它监视的数据模型（Model），因此应该事先在被它监视的数据那里注册。如Spring 的 DispatcherServlet。
- 3)控制器（Controller）起到不同层面间的组织作用，用于控制应用程序的流程。它处理事件并作出响应。“事件”包括用户的行为和数据 Model 上的改变。

## 12. 什么是 Java 优先级队列。
PriorityQueue类在Java1.5中引入。PriorityQueue是基于优先堆的一个无界队列，这个优先队列中的元素可以默认自然排序或者通过提供的Comparator（比较器）在队列实例化的时排序。
具体取决于使用哪个构造函数。优先级队列不允许空元素。依靠自然排序的优先级队列也不允许插入不可比较的对象（否则可能导致ClassCastException）。
优先队列的头是基于自然排序或者Comparator排序的最小元素。如果有多个对象拥有同样的排序，那么就可能随机地取其中任意一个。当我们获取队列时，返回队列的头对象。
PriorityQueue是非线程安全的，所以Java提供了PriorityBlockingQueue
## 13. 简述一下 spring，都用过 spring 的什么？
Spring Framework 是一个开源的Java／Java EE全功能栈（full-stack）的应用程序框架，以Apache许可证形式发布，也有.NET平台上的移植版本.
Spring Framework提供了一个简易的开发方式，这种开发方式，将避免那些可能致使底层代码变得繁杂混乱的大量的属性文件和帮助类。
常见的有:spring-aop,spring-jdbc,spring-tx,spring-jms,spring-data,spring-data-jpa,spring-data-redis,spring-orm,springmvc,spring-security,springboot,spring-batch
## 14. 说一下数据库的索引。数据库隔离级别。
### 14.1数据库索引
索引是对数据库表中的一列或多列的值，进行排序的一种结构 ，使用索引可以快速访问数据库表中的特定信息，是加快数据库查询的技术。
索引的优缺点
优点
- 1.索引可以避免全表扫描；
- 2.大大提高数据检索的速度
缺点
- 1.需要耗费时间的，这种时间会随着数据量的增加而增加
- 2.当表中的数据进行增加、删除和修改的时候，索引也要动态地维护，这样就降低了数据的维护速度
索引类型
- 1.normal：表示普通索引
- 2.unique：表示唯一的，不允许重复的索引。
- 3.full textl: 表示 全文搜索的索引。 
索引结构
- 1.Hash索引:哈希索引只有Memory, NDB两种引擎支持，Memory引擎默认支持哈希索引，如果多个hash值相同，出现哈希碰撞，那么索引以链表方式存储。
	哈希索引就是采用一定的哈希算法，把键值换算成新的哈希值，检索时不需要类似B+树那样从根节点到叶子节点逐级查找，只需一次哈希算法即可立刻定位到相应的位置，速度非常快。
- 2.B-Tree索引:最为频繁的索引类型，除了 Archive 存储引擎之外的其他所有的存储引擎都支持 B-Tree 索引
- 3.oracle有位图索引。适用于选择基数小的列。

### 14.2数据库隔离级别

	事务隔离（英语：Transaction Isolation）定义了数据库系统中一个操作的结果在何时以何种方式对其他并发操作可见。
	隔离是事务ACID（原子性、一致性性、隔离性、持久性）四大属性之一。
- 1.未提交读（READ UNCOMMITTED）是最低的隔离级别。允许“脏读”（dirty reads），事务可以看到其他事务“尚未提交”的修改。
- 2.提交读（READ COMMITTED） 基于锁机制并发控制的DBMS需要对选定对象的写锁一直保持到事务结束，但是读锁在SELECT操作完成后马上释放。“不可重复读”现象可能会发生。
- 3.可重复读（REPEATABLE READS）基于锁机制并发控制的DBMS需要对选定对象的读锁（read locks）和写锁（write locks）一直保持到事务结束，但不要求“范围锁”，因此可能会发生“幻影读”
- 4.可序列化 是最低的隔离级别。允许“脏读”（dirty reads），事务可以看到其他事务“尚未提交”的修改。要求在选定对象上的读锁和写锁保持直到事务结束后才能释放。
	在SELECT 的查询中使用一个“WHERE”子句来描述一个范围时应该获得一个“范围锁”（range-locks）。这种机制可以避免“幻影读”（phantom reads）现象

隔离级别vs 锁持续时间
在基于锁的并发控制中，隔离级别决定了锁的持有时间。"C"-表示锁会持续到事务提交。 "S" –表示锁持续到当前语句执行完毕。
如果锁在语句执行完毕就释放则另外一个事务就可以在这个事务提交前修改锁定的数据，从而造成混乱。

|  隔离级别l	|	写操作	|  	读操作	|	范围操作 				|
| ------------- |:---------:| -----:  	| ------------------:		|
|  未提交读 	|	S 		|  	S 		|	S 						|
|  提交读	  	|   C  		|    S 		|	S 						|
|  可重复读 	|、 C 		|    C 		|   S 						|
|  可序列化  	|   C 		|    C		|   C						|

不同的DBMS默认隔离级别也不同。大多数据库允许用户设置隔离级别
```
transaction-isolation = {READ-UNCOMMITTED | READ-COMMITTED | REPEATABLE-READ | SERIALIZABLE}
oracle默认级别为：READ-COMMITTED
InnoDB默认级别为：REPEATABLE-READ
```
## 15.statement 与 PreparedStatement 的区别，如何防止 sql 注入。
### 15.1
- 1.Statement可以正常访问数据库，适用于运行静态 SQL 语句。 Statement 接口不接受参数。
- 2.PreparedStatement预编译的,运行时接受输入的参数,适用于批量处理
- 3.PreparedStatement 对象的开销比Statement大，对于一次性操作并不会带来额外的好处。
- 4.PreparedStatement对象的参数可以被强制进行类型转换，更安全
### 15.2
SQL注入攻击（SQL Injection），简称注入攻击，是Web开发中最常见的一种安全漏洞。
可以用它来从数据库获取敏感信息，或者利用数据库的特性执行添加用户，导出文件等一系列恶意操作，甚至有可能获取数据库乃至系统用户最高权限。

- 1.	严格限制Web应用的数据库的操作权限，给此用户提供仅仅能够满足其工作的最低权限，从而最大限度的减少注入攻击对数据库的危害。
- 2.    检查输入的数据是否具有所期望的数据格式，严格限制变量的类型，例如使用regexp包进行一些匹配处理，或者使用strconv包对字符串转化成其他基本类型的数据进行判断。
- 3.    对进入数据库的特殊字符（'"\尖括号&*;等）进行转义处理，或编码转换。Go 的text/template包里面的HTMLEscapeString函数可以对字符串进行转义处理。
- 4.    所有的查询语句建议使用数据库提供的参数化查询接口，参数化的语句使用参数而不是将用户输入变量嵌入到SQL语句中，即不要直接拼接SQL语句。例如使用database/sql里面的查询函数Prepare和Query，或者Exec(query string, args ...interface{})。
- 5.    在应用发布之前建议使用专业的SQL注入检测工具进行检测，以及时修补被发现的SQL注入漏洞。网上有很多这方面的开源工具，例如sqlmap、SQLninja等。
- 6.    避免网站打印出SQL错误信息，比如类型错误、字段不匹配等，把代码里的SQL语句暴露出来，以防止攻击者利用这些错误信息进行SQL注入。

## 16. 简述一下 restful，设计一个 url 要注意什么。
- 1.规划好API的外观要先于开发它实际的功能
- 2.API应该尽可能通过抽象来分离数据与业务逻辑
- 3.API根入口点保持尽可能的简单是很重要
- 4.API分析就是持续跟踪那些正为人使用的API的版本和端点信息
- 5.将API的版本号放入URL
- 6.网址中不能有动词，只能有名词
- 7.对于资源的具体操作类型，由HTTP动词表示
- 8.参照资源的关系设计
- 9.API应该提供参数，过滤返回结果
- 10.基于HTTPS来发布
- 11.向用户返回的状态码和提示信息
- 12.尽量JSON
- 13.API的身份认证
## 17. 如何进行单元测试的。
JUnit是一个回归测试框架。Junit测试是程序员测试，即所谓白盒测试。
### 17.1 如何确定单元测试
- 1.一个单元测试基本是以一个对象的明确特性为基础，应该限定在一个明确的线程范围内。
- 2.测试单元应该以一个对象的内部状态的转换为基本编写单元
- 3.并不是所有的对象组特征都需要被编写成独立的测试单元，对象组特征里筛选有价值的测试单元，应该在有可能引入错误的地方引入测试单元。
	通常这些地方存在于有特定边界条件、复杂算法以及需求变动比较频繁的代码逻辑中
- 4.根据需求的变化不断的演变。修改类的行为规则，针对这个类的测试单元进行修改，以适应变化	
### 17.2 编写过程
- 1	首先分析出状态的变化过程（状态转换图对这个过程的描述非常清晰），
- 2	然后根据状态的定义确定分析的状态数据，
- 3	最后是提供这些内部的状态数据的访问。
## 18. 选用了 base 跟 solo，如何实现的数据同步。
## 19. 说几个常用算法。

## 21. 简述 form 表单提交 POST 方法与 GET 方法在字符编码,http 协议等方面的区别。
## 22.ArrayList，LinkedList，HashMap 的区别。
## 23. 介绍一下 Spring 的事务管理，使用什么设计模式实现。
## 24. 一个 HTTP 请求从开始到结束都经历哪些过程，简写流程图即可。
## 25.synchronize 关键字与 volatile 关键字的作用和区别。
## 26. 说一下内连接，左连接，右连接。
## 27. 给 list 排序（我记得是有个 collections.sort），说出这个，又问了一个什么排序的，忘记了。
## 28. 写两个链表，将其合并排序，如何操作不多占用内存。（完全没任何思路，对链表就不熟哇···）
## 29. 多线程是 void，无返回值的，如果用多线程从不同的数据库中读取到数据，如何将读取到的信息合并
## 30. 写出单例模式。
## 1、Spring.mvc 的优势，原理，流程
## 2、Mybatis 的原理优势
## 3、集合里面那些对象的原理
## 4、扩容原理，特别是 map 的底层
## 5、Hashmap、Hashtable 和 cocurrentHashMap 的区别，要讲出它们各自的实现原理才行，比如 Hashmap 的扩容机制、cocurrentHashMap 的桶分割原理、多线程安全性。
## 6、几种造线程池的方法，区别
## 7、Rpc 原理
## 8、Nio 和 netty，常用的接口
## 9、Redis 和数据库的持久化的
## 10、Memached 过程和原理
## 11、多线程时间复杂度
## 12、Redis 做队列的原理
## 13、zk 做订阅的原理，底层
## 14、Juc 里面的锁原理
## 15、实现自己的 hashmap
## 16、treemap 红黑树
## 17、jvm 调优
## 18、jvm 内存模型
## 19、类加载器机制
## 20、数据库索引
## 21、数据破坏索引
## 22、手写快排
## 23、js 闭包
## 24、nio 是否了解 阻塞之后通知机制是怎样的？
## 25、Java 的序列化做什么用的 序列化 id 会出现哪些问题？
## 26、 在 Java 中 Executor 和 Executors 的区别？
- Executors 类提供工厂方法用来创建不同类型的线程池。
- Executor Java JUC的核心接口，用来并发执行提交的任务。
## 27、 为什么使用 Executor 框架比使用应用创建和管理线程好？
## 28、怎么通过 linux 命令去分析 jvm 里面那个线程阻塞了
## 29、Java 中用到的线程调度算法是什么？
一般线程调度模式分为两种:抢占式调度和协同式调度。
抢占式。一个线程用完CPU之后，操作系统会根据线程优先级、线程饥饿情况等数据算出一个总的优先级并分配下一个时间片给某个线程执行。
- 抢占式调度指的是每条线程执行的时间、线程的切换都由系统控制，系统控制指的是在系统某种运行机制下，可能每条线程都分同样的执行时间片，也可能是某些线程执行的时间片较长，
甚至某些线程得不到执行的时间片。在这种机制下，一个线程的堵塞不会导致整个进程堵塞。

- 协同式调度指某一线程执行完后主动通知系统切换到另一线程上执行，这种模式就像接力赛一样，一个人跑完自己的路程就把接力棒交接给下一个人，下个人继续往下跑。
线程的执行时间由线程本身控制，线程切换可以预知，不存在多线程同步问题，但它有一个致命弱点：如果一个线程编写有问题，运行到一半就一直堵塞，那么可能导致整个系统崩溃。

Java使用的线程调度是抢占式调度

## 30、什么是多线程中的上下文切换？
- 上下文是指某一时间点 CPU寄存器和程序计数器的内容。寄存器是CPU内部的数量较少但是速度很快的内存。
- 寄存器通过对常用值（通常是运算的中间值）的快速访问来提高计算机程序运行的速度。
- 程序计数器是一个专用的寄存器，用于表明指令序列中 CPU正在执行的位置，存的值为正在执行的指令的位置或下一个将要被执行的指令的位置。
- 上下文切换是指 CPU 从一个进程或线程切换到另一个进程或线程。

*上下文切换活动*
-	（1）挂起一个进程，将这个进程在 CPU 中的状态（上下文）存储于内存中的某处，
-	（2）在内存中检索下一个进程的上下文并将其在 CPU 的寄存器中恢复，
-	（3）跳转到程序计数器所指向的位置（即跳转到进程被中断时的代码行),以恢复该进程。

## 31、classloader 结构，是否可以自己定义一个 java.lang.String 类，为什么？ 双亲代理机制。
## 32、有没有做过 jvm 内存调优，如何做的，举例子，用过哪些工具？
## 33、Java 中的 volatile 关键是什么作用？怎样使用它？在 Java 中它跟 synchronized 方法有什么不同？

## 35、 介绍 Java 中垃圾回收机制，程序员平时需要关注这个吗？为什么？请举例说明。
Java 语言的一大特点就是可以进行自动垃圾回收处理。垃圾回收可以有效的防止内存泄露，有效的使用空闲的内存。
### 35.1 对象存活的判定

	对象存活判定,常见的方法有引用计数（Reference Counting）有可达性分析（Reachability Analysis）两种。
	JAVA使用可达性分析来判定对象是否存活的。
	基本思路就是通过一系列的称为GC根节点（GC Roots）的对象作为起始点，从这些节点开始进行向下搜索，搜索所走过的路径成为引用链（Reference Chain）.
	当一个对象到GC Roots没有任何引用链相连（用图论的话来说就是从GC Roots到这个对象不可达）时，则证明此对象是不可用的。
	
*常见枚举根节点*
	
- 	虚拟机栈（栈帧中的本地变量表）中引用的对象
-   方法区中类静态属性引用的对象
-   方法区中常量引用的对象
-   本地方法栈中JNI（即一般说的Native方法）引用的对象

### 35.2 常见算法
- 标记-清除算法 (Mark-Sweep):分为两个阶段：标记阶段和清除阶段。
	- 标记阶段首先通过根节点，标记所有从根节点开始的较大对象。
	- 在清除阶段，清除所有未被标记的对象。
	- 该算法最大的问题是存在大量的空间碎片
- 复制算法 (Copying):现有的内存空间分为两快，每次只使用其中一块，在垃圾回收时将正在使用的内存中的存活对象复制到未被使用的内存块中，
	之后，清除正在使用的内存块中的所有对象，交换两个内存的角色，完成垃圾回收。
- 标记-压缩算法 (Mark-Compact):可达对象做一次标记之后，将所有的存活对象压缩到内存的一端。之后，清理边界外所有的空间。
	这种方法既避免了碎片的产生，又不需要两块相同的内存空间，因此，其性价比比较高。
- 增量算法 (Incremental Collecting):如果一次性将所有的垃圾进行处理，需要造成系统长时间的停顿，那么就可以让垃圾收集线程和应用程序线程交替执行.
	但是，因为线程切换和上下文转换的消耗，会使得垃圾回收的总体成本上升,造成系统吞吐量的下降。
- 分代 (Generational Collecting):不同阶段最优的方式是使用合适的算法用于本阶段的垃圾回收
### 35.3 垃圾收集器
-	1. 按线程数分，可以分为串行垃圾回收器和并行垃圾回收器。
-	2. 按照工作模式分，可以分为并发式垃圾回收器和独占式垃圾回收器。
-	3. 按碎片处理方式可分为压缩式垃圾回收器和非压缩式垃圾回收器。
-	4. 按工作的内存区间，又可分为新生代垃圾回收器和老年代垃圾回收器。
评价一个垃圾处理器的好坏。
-	吞吐量：指在应用程序的生命周期内，应用程序所花费的时间和系统总运行时间的比值。
-	垃圾回收器负载：和吞吐量相反，
-	停顿时间：指垃圾回收器正在运行时，应用程序的暂停时间。
-	垃圾回收频率：指垃圾回收器多长时间会运行一次。
-	反应时间：指当一个对象被称为垃圾后多长时间内，它所占据的内存空间会被释放。
-	堆分配：不同的垃圾回收器对堆内存的分配方式可能是不同的。

### 35.4 分代

![Garbage_Collection_and](https://1.bp.blogspot.com/-ZiJiWwHc54A/VvPOdZJoV7I/AAAAAAAAFQA/GvxtW0r2SuQgvCQAKLYj7X_8f2HpdwAtg/s640/Garbage%2BCollection%2Band%2BJVM%2Bparameters.jpg)

![Garbage%2BCollection_heap](https://4.bp.blogspot.com/-id4mr-lULDI/VvPOd3L964I/AAAAAAAAFQI/CJyyQuxaWgkITVpkXVI0diN93HtsRfxWg/s640/Java%2BGarbage%2BCollection%2Bheap.png)
		
## 37、override 和 overload 的区别。
## 38、求二叉树的最大距离（即相距最远的两个叶子节点），写代码。
## 39、 两个栈实现一个队列，写代码。
## 40、 你觉得你的优势是什么？有什么技术薄弱点吗？
## 41、数据库 sql 调优，慢 sql 定位
## 42、索引有哪几种，区别，使用场景
## 43、mysql 引擎，哪几种，区别使用场景

|  mysql 引擎	|	特点	|  	场景	|
| ------------- |:----------:| :-----   |
|  MyISAM 		|	基于ISAM数据库引擎,基于表锁控制并发，延迟插入，读写互相阻塞；只会缓存索引; 支持三种不同的存储结构：静态型、动态型、压缩型		|  	不需要事务支持，并发度低 		|
|  InnoDB	  	|  提供了ACID事务支持、系统崩溃修复能力和行级锁（MVCC)并发控制，不支持全文搜索  		|    并发度较高的场景		|
|  HEAP 		|  磁盘文件只存储表的结构，而其数据存储在内存中 ,极高的插入、更新和查询效率		|   如果需要该数据库中一个用于查询的临时表。 		|
|  Archive  	|   提供了压缩功能，高效的插入速度 ,不支持索引,不支持update和delete操作		|    用于数据归档		|
|  Cluster/NDB  |   多台数据机器联合提供服务以提高整体性能和安全性;分布式，支持事务 		|    数据量大、安全和性能要求高的场景		|

## 45、linux shell脚本的使用，统计，排序等等 
## 46、linux 常用命令，例如top命令查看进程的后每个参数的意义 
## 47、乐观锁和悲观锁 
## 48、nginx的配置 
## 49、你遇到的OOM问题，怎么解决的。 
## 50、你在项目中遇到过那些高并发的问题，怎么解决的。 
## 51、谈谈常见的负载均衡策略 分别有什么优缺点，用过哪些 
## 52、jdk\bin下的工具你用过哪些