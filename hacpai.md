## 1.java 中的关键字 final 可以用来修饰什么，分别起什么作用。
	final 表示"不可变",可以用来修饰类，属性，和变量。
	- 1)修饰类：表示类不可被继承；常见的如Integer.java,Float.java,String.class。
	- 2)修饰类属性:表示不能修改，必须在实例初始化之前进行初始化。一般使用于不变(Immutable)模式中，在并发设计中，不变对象是线程安全的，降低并发编程复杂度。
	- 3)修饰局部变量：同样表示变量不允许修改，一般使用在匿名内部类参数;但是如果修饰变量为数组或引用类型时，仅仅表示对象引用不可变，但对象值域是仍然可变的。
## 2.请说明 ArrayList，Vector，LinkedList 的存档性能和特性。
	- 1) 都是有序集合接口java.util.List的的实现。
	- 2）Vector和ArrayList底层实现都是Object[]数组。支持索引随机访问元素。区别是Vector通过将方法声明为synchronized方法，实现线程安全，所以,Vector相对ArrayList,
		 性能要差。
	- 3）LinkedList，使用链表结构实现，
## 3.String，StringBuffer，StringBuilder 有什么区别。
## 4.swith 是否能作用在 byte 上，是否能作用在 long 上，是否能作用在 strng 上。
## 5. 存在表 T（a,b,c,d），要根据字段 c 排序后取第 21-30 条记录显示，请写出 sql 文。
## 6. 查出 user 表中 username 相同的记录，显示 username 和重复的次数，给出 sql。
## 7.float 是多少位的。
## 8. 设计四个线程，其中两个线程每次对 J 增加 1，另外两个线程每次对 J 减 1，写出程序或者思路。
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