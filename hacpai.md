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
## 5. 存在表 T（a,b,c,d），要根据字段 c 排序后取第 21-30 条记录显示，请写出 sql 文。
## 6. 查出 user 表中 username 相同的记录，显示 username 和重复的次数，给出 sql。
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
## 10. 写出 hashMap 的数据结构。
## 11. 简述 MVC 设计模式。
## 12. 什么是 Java 优先级队列。
## 13. 简述一下 spring，都用过 spring 的什么？
## 14. 说一下数据库的索引。数据库隔离级别。
## 15.statement 与 PreparedStatement 的区别，如何防止 sql 注入。
## 16. 简述一下 restful，设计一个 url 要注意什么。
## 17. 如何进行单元测试的。
## 18. 选用了 base 跟 solo，如何实现的数据同步。
## 19. 说几个常用算法。