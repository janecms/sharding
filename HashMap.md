# HashMap
HashMap的一个实例有两个影响其性能的参数：初始容量和负载因子。容量是哈希表中桶的数量，初始容量就是哈希表创建时的容量。
加载因子是散列表在其容量自动增加之前被允许得到的度量。当哈希表中的条目数量超过了负载因子和当前容量的乘积时，
散列表就被重新映射（即内部数据结构被重建），这样散列表大约有两个桶的数量。

![](https://tech.meituan.com/img/java-hashmap/hashMap%E5%86%85%E5%AD%98%E7%BB%93%E6%9E%84%E5%9B%BE.png)
```
//默认容量
static final int DEFAULT_INITIAL_CAPACITY = 1 << 4;
//最大容量
static final int MAXIMUM_CAPACITY = 1 << 30;
//默认加载因子
static final float DEFAULT_LOAD_FACTOR = 0.75f;
//链表转成红黑树的阈值
static final int TREEIFY_THRESHOLD = 8;
//红黑树转为链表的阈值
static final int UNTREEIFY_THRESHOLD = 6;
//存储方式由链表转成红黑树的容量的最小阈值
static final int MIN_TREEIFY_CAPACITY = 64;
//HashMap中存储的键值对的数量
transient int size;
//空的存储实体  
transient Entry<K,V>[] table = (Entry<K,V>[]) EMPTY_TABLE; 
//用于快速失败，由于HashMap非线程安全，在对HashMap进行迭代时，如果期间其他线程的参与导致HashMap的结构发生变化了（比如put，remove等操作），
//需要抛出异常ConcurrentModificationException
transient int modCount;

//扩容阈值，当size>=threshold时，就会扩容
int threshold;
//HashMap的加载因子
final float loadFactor;

```
## put

![](https://tech.meituan.com/img/java-hashmap/hashMap%20put%E6%96%B9%E6%B3%95%E6%89%A7%E8%A1%8C%E6%B5%81%E7%A8%8B%E5%9B%BE.png)


```
JDK1.8HashMap的put方法源码如下:

 public V put(K key, V value) {
     // 对key的hashCode()做hash
     return putVal(hash(key), key, value, false, true);
 }
 
 final V putVal(int hash, K key, V value, boolean onlyIfAbsent,
                boolean evict) {
     Node<K,V>[] tab; Node<K,V> p; int n, i;
     // 步骤①：tab为空则创建
     if ((tab = table) == null || (n = tab.length) == 0)
         n = (tab = resize()).length;
     // 步骤②：计算index，并对null做处理 
     if ((p = tab[i = (n - 1) & hash]) == null) 
         tab[i] = newNode(hash, key, value, null);
     else {
         Node<K,V> e; K k;
         // 步骤③：节点key存在，直接覆盖value
         if (p.hash == hash &&
             ((k = p.key) == key || (key != null && key.equals(k))))
             e = p;
         // 步骤④：判断该链为红黑树
         else if (p instanceof TreeNode)
             e = ((TreeNode<K,V>)p).putTreeVal(this, tab, hash, key, value);
         // 步骤⑤：该链为链表
         else {
             for (int binCount = 0; ; ++binCount) {
                 if ((e = p.next) == null) {
                     p.next = newNode(hash, key,value,null);
                      //链表长度大于8转换为红黑树进行处理
                     if (binCount >= TREEIFY_THRESHOLD - 1) // -1 for 1st  
                         treeifyBin(tab, hash);
                     break;
                 }
                  // key已经存在直接覆盖value
                 if (e.hash == hash &&
                     ((k = e.key) == key || (key != null && key.equals(k)))) 
                            break;
                 p = e;
             }
         }
         
         if (e != null) { // existing mapping for key
             V oldValue = e.value;
             if (!onlyIfAbsent || oldValue == null)
                 e.value = value;
             afterNodeAccess(e);
             return oldValue;
         }
     }

     ++modCount;
     // 步骤⑥：超过最大容量 就扩容
     if (++size > threshold)
         resize();
     afterNodeInsertion(evict);
     return null;
 }
```

①.判断键值对数组table[i]是否为空或为null，否则执行resize()进行扩容；

②.根据键值key计算hash值得到插入的数组索引i，如果table[i]==null，直接新建节点添加，转向⑥，如果table[i]不为空，转向③；

③.判断table[i]的首个元素是否和key一样，如果相同直接覆盖value，否则转向④，这里的相同指的是hashCode以及equals；

④.判断table[i] 是否为treeNode，即table[i] 是否是红黑树，如果是红黑树，则直接在树中插入键值对，否则转向⑤；

⑤.遍历table[i]，判断链表长度是否大于8，大于8的话把链表转换为红黑树，在红黑树中执行插入操作，否则进行链表的插入操作；遍历过程中若发现key已经存在直接覆盖value即可；

⑥.插入成功后，判断实际存在的键值对数量size是否超多了最大容量threshold，如果超过，进行扩容。

------------------
# ConcurrentHashMap

ConcurrentHashMap 类中包含两个静态内部类 HashEntry 和 Segment。
- HashEntry 用来封装映射表的键/值对；
- Segment 用来充当锁的角色，每个 Segment 对象守护整个散列映射表的若干个桶。每个桶是由若干个 HashEntry 对象链接起来的链表。一个 ConcurrentHashMap 实例中包含由若干个 Segment 对象组成的数组。
JDK1.6
![](https://www.ibm.com/developerworks/cn/java/java-lo-concurrenthashmap/image004.jpg)
static final class Segment<K,V> extends ReentrantLock implements Serializable { 
       /** 
        * 在本 segment 范围内，包含的 HashEntry 元素的个数
        * 该变量被声明为 volatile 型
        */ 
       transient volatile int count; 
 
       /** 
        * table 被更新的次数
        */ 
       transient int modCount; 
 
       /** 
        * 当 table 中包含的 HashEntry 元素的个数超过本变量值时，触发 table 的再散列
        */ 
       transient int threshold; 
 
       /** 
        * table 是由 HashEntry 对象组成的数组
        * 如果散列时发生碰撞，碰撞的 HashEntry 对象就以链表的形式链接成一个链表
        * table 数组的数组成员代表散列映射表的一个桶
        * 每个 table 守护整个 ConcurrentHashMap 包含桶总数的一部分
        * 如果并发级别为 16，table 则守护 ConcurrentHashMap 包含的桶总数的 1/16 
        */ 
       transient volatile HashEntry<K,V>[] table; 
 
       /** 
        * 装载因子
        */ 
       final float loadFactor; 
 
       Segment(int initialCapacity, float lf) { 
           loadFactor = lf; 
           setTable(HashEntry.<K,V>newArray(initialCapacity)); 
       } 
 
       /** 
        * 设置 table 引用到这个新生成的 HashEntry 数组
        * 只能在持有锁或构造函数中调用本方法
        */ 
       void setTable(HashEntry<K,V>[] newTable) { 
           // 计算临界阀值为新数组的长度与装载因子的乘积
           threshold = (int)(newTable.length * loadFactor); 
           table = newTable; 
       } 
 
       /** 
        * 根据 key 的散列值，找到 table 中对应的那个桶（table 数组的某个数组成员）
        */ 
       HashEntry<K,V> getFirst(int hash) { 
           HashEntry<K,V>[] tab = table; 
           // 把散列值与 table 数组长度减 1 的值相“与”，
// 得到散列值对应的 table 数组的下标
           // 然后返回 table 数组中此下标对应的 HashEntry 元素
           return tab[hash & (tab.length - 1)]; 
       } 
}
```

1.8的实现已经抛弃了Segment分段锁机制，利用CAS+Synchronized来保证并发更新的安全，底层依然采用数组+链表+红黑树的存储结构。

![](http://img.voidcn.com/vcimg/000/005/607/054_9d4_a08.png)
```

CAS算法；unsafe.compareAndSwapInt(this, valueOffset, expect, update);  CAS(Compare And Swap)，
- 如果valueOffset位置包含的值与expect值相同，则更新valueOffset位置的值为update，并返回true，
- 否则不更新，返回false。

与Java8的HashMap有相通之处，底层依然由“数组”+链表+红黑树；
底层结构存放的是TreeBin对象，而不是TreeNode对象；
CAS作为知名无锁算法，那ConcurrentHashMap就没用锁了么？
当然不是，hash值相同的链表的头结点还是会synchronized上锁。 