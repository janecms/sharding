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
| ------------- |:----------:| -----:  | ------------------:		|
|  未提交读 	|	S 		|  	S 		|	S 						|
|  提交读	  	|   C  		|    S 		|	S 						|
|  可重复读 	|、 C 		|    C 		|   S 						|
|  可序列化  	|   C 		|    C		|   C						|



## 15.statement 与 PreparedStatement 的区别，如何防止 sql 注入。
## 16. 简述一下 restful，设计一个 url 要注意什么。
## 17. 如何进行单元测试的。
## 18. 选用了 base 跟 solo，如何实现的数据同步。
## 19. 说几个常用算法。