## 25.synchronize 关键字与 volatile 关键字的作用和区别。
### 不同点
-	volatile 变量是一种稍弱的同步机制，在访问 volatile 变量时不会执行加锁操作，因此也就不会使执行线程阻塞，
	因此 volatile 变量是一种比 synchronized 关键字更轻量级的同步机制。
-	从内存可见性的角度看，写入 volatile 变量相当于退出同步代码块，而读取 volatile 变量相当于进入同步代码块。	
-	加锁机制（即同步机制）既可以确保可见性又可以确保原子性，而 volatile 变量只能确保可见性
-	volatile是变量修饰符，而synchronized则作用于一段代码或方法。
-	 volatile只是在线程内存和“主”内存间同步某个变量的值；而synchronized通过锁定和解锁某个监视器同步所有变量的值。
		显然synchronized要比volatile消耗更多资源。 
### 相同点
-	两者都实现了内存可见性，影响重排序;