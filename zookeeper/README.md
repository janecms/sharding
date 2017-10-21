ZooKeeper是分布式应用程序的高性能协调服务。提供常见的服务，如命名，配置管理，同步和组服务。

#  ZooKeeper Overview 
## ZooKeeper是分布式，开放源码的分布式应用协调服务。
它暴露了一组简单的原语，分布式应用程序可以基于实现更高级别的服务进行同步，配置维护以及组和命名。
它被设计为易于编程，并使用在文件系统熟悉的**目录树结构**的数据模型。
它运行在Java中，并且具有Java和C的绑定。

协调服务是非常难以正确的。他们特别容易出现诸如竞态条件和死锁等错误。 
ZooKeeper背后的动机是缓解分布式应用程序从头开始执行协调服务的责任。

## 设计目标

ZooKeeper很简单ZooKeeper允许分布式进程通过与标准文件系统类似的共享层次命名空间相互协调。名称空间由ZooKeeper语法中的数据寄存器（称为znodes）组成，这些类似于文件和目录。
与专为存储设计的典型文件系统不同，ZooKeeper实现对高性能，高可用性，严格有序的访问非常重要。 

ZooKeeper的性能方面意味着它可以在大型分布式系统中使用。可靠性方面使其不能成为单点故障。严格的排序意味着复杂的同步原语可以在客户端实现。

ZooKeeper被复制。像它所协调的分布式进程一样，ZooKeeper本身就是为了复制一组被称为合奏的主机。

![](http://zookeeper.apache.org/doc/current/images/zkservice.jpg)

构成ZooKeeper服务的服务器必须彼此了解。 它们保持状态的内存映像，以及持久存储中的事务日志和快照。 只要大多数服务器可用，ZooKeeper服务将可用。

客户端连接到一个ZooKeeper服务器。 客户端维护TCP连接，通过它发送请求，获取响应，获取watch事件并发送心跳。 如果与服务器的TCP连接断开，客户端将连接到不同的服务器。

ZooKeeper 是顺序的。 ZooKeeper将每个更新标记为反映所有ZooKeeper事务顺序的数字。 后续操作可以使用该命令来实现更高级别的抽象，例如同步原语。

ZooKeeper很快。 它在“读主导”工作负载中特别快。 ZooKeeper应用程序在数千台机器上运行，并且在写入次数比写入次数大概为10：1时，性能最好。

**数据模型和层次命名空间**
ZooKeeper提供的名称空间与标准文件系统类似。 名称是以斜杠（/）分隔的路径元素序列。 ZooKeeper的名称空间中的每个节点都由路径标识。

![](http://zookeeper.apache.org/doc/current/images/zknamespace.jpg)

- 节点和临时节点
与标准文件系统不同，ZooKeeper命名空间中的每个节点都可以具有与其相关联的数据以及子节点。它就像有一个允许文件也是一个目录的文件系统。 （ZooKeeper设计用于存储协调数据：状态信息，配置，位置信息等，因此存储在每个节点上的数据通常很小，字节到千字节范围。）我们使用术语znode来表明我们正在谈论ZooKeeper数据节点。

Znodes维护一个统计结构，其中包括数据更改，ACL更改和时间戳的版本号，以允许缓存验证和协调更新。每次znode的数据发生变化时，版本号都会增加。例如，每当客户端检索数据时，它也会收到数据的版本。

存储在命名空间中每个znode处的数据以原子方式读取和写入。读取获取与znode相关联的所有数据字节，写入替换所有数据。每个节点都有一个访问控制列表（ACL），它限制谁能做什么。

ZooKeeper还具有短暂节点的概念。只要创建znode的会话处于活动状态，就会存在这些znodes。当会话结束时，znode被删除，临时节点很有用。

## 条件更新和Watch

ZooKeeper支持Watch的概念。 客户端可以在znode上设置Watch。 当znode更改时，Watch将被触发并移除。 当手表触发时，客户端收到一个数据包，说明znode已经改变了。 如果客户端与ZooKeeper服务器之间的连接断开，客户端将收到本地通知。 这些可以用于[tbd]。

## 保证
ZooKeeper非常快速，非常简单。 由于目标是为建设更为复杂的服务，如同步化的基础，它提供了一套保证。 这些是：

- 顺序一致性 - 客户端的更新将按照发送的顺序进行应用。

- 原子性 - 更新成功或失败。 没有部分结果。

- 单一系统映像 - 客户端将看到与服务器连接的服务相同的服务视图。

- 可靠性 - 一旦应用了更新，它将从当前持续到客户端覆盖更新。

- 及时性 - 系统的客户端视图在一定时间内保证是最新的。

## 简单的API
ZooKeeper的设计目标之一是提供一个非常简单的编程接口。 因此，它仅支持以下操作：

- create 在树中的某个位置创建一个节点
- delete 删除一个节点
- exists 测试一个节点是否存在于某个位置
- get data  从节点读取数据
- set data 将数据写入节点
- get children 检索节点的子节点列表
- sync 等待数据传播

## 履行

ZooKeeper组件显示ZooKeeper服务的高级组件。 除了请求处理器之外，组成ZooKeeper服务的每个服务器都会复制每个组件的自己的副本。
![](http://zookeeper.apache.org/doc/current/images/zkcomponents.jpg)

复制数据库是包含整个数据树的内存数据库。将更新记录到磁盘以获取可恢复性，并将写入序列化到磁盘，然后再将其应用于内存数据库。

每个ZooKeeper服务器都为客户端服务。客户端连接到一个服务器以提交irequests。读取请求由每个服务器数据库的本地副本服务。更改服务状态，写入请求的请求由agreement协议进行处理。

作为协议协议的一部分，客户端的所有写入请求都将转发到单个服务器，称为leader。称为followers的其他ZooKeeper服务器从leader接收消息提议，并同意消息传递。消息传递层负责替代领导者的失败，并与领导者同步追随者。

ZooKeeper使用自定义原子消息协议。由于消息传递层是原子的，所以ZooKeeper可以保证本地副本不会发散。当领导者收到写请求时，它会计算要应用写入时系统的状态，并将其转换为捕获此新状态的事务。

# ZooKeeper Getting Started Guide

- Standalone Operation
  - 需要一个配置文件  conf/zoo.cfg
  ```
	tickTime=2000
	dataDir=/var/lib/zookeeper
	clientPort=2181  
  ```
tickTime ZooKeeper使用的基本时间单位（毫秒）。 它用于做心跳，最小会话超时将是tickTime的两倍。
dataDir 存储内存数据库快照的位置，除非另有规定，更新数据库的事务日志。
clientPort 端口监听客户端连接 

```
bin/zkServer.sh start
```
ZooKeeper使用log4j记录消息 .

## Managing ZooKeeper Storage

- Connecting to ZooKeeper
```
$ bin/zkCli.sh -server 127.0.0.1:2181
```

```
[zkshell: 0] help

输入简单命令
[zkshell: 8] ls /
[zookeeper]

[zkshell: 9] create /zk_test my_data
Created /zk_test

[zkshell: 11] ls /
[zookeeper, zk_test]

[zkshell: 12] get /zk_test
my_data
cZxid = 5
ctime = Fri Jun 05 13:57:06 PDT 2009
mZxid = 5
mtime = Fri Jun 05 13:57:06 PDT 2009
pZxid = 5
cversion = 0
dataVersion = 0
aclVersion = 0
ephemeralOwner = 0
dataLength = 7
numChildren = 0

[zkshell: 14] set /zk_test junk
cZxid = 5
ctime = Fri Jun 05 13:57:06 PDT 2009
mZxid = 6
mtime = Fri Jun 05 14:01:52 PDT 2009
pZxid = 5
cversion = 0
dataVersion = 1
aclVersion = 0
ephemeralOwner = 0
dataLength = 4
numChildren = 0

[zkshell: 15] get /zk_test
junk
cZxid = 5
ctime = Fri Jun 05 13:57:06 PDT 2009
mZxid = 6
mtime = Fri Jun 05 14:01:52 PDT 2009
pZxid = 5
cversion = 0
dataVersion = 1
aclVersion = 0
ephemeralOwner = 0
dataLength = 4
numChildren = 0


[zkshell: 16] delete /zk_test
[zkshell: 17] ls /
[zookeeper]
```

## Running Replicated ZooKeeper
以独立模式运行ZooKeeper，便于评估，开发和测试。 但在生产中，您应该以复制模式运行ZooKeeper。 同一应用程序中的复制服务器组称为仲裁，而在复制模式下，仲裁中的所有服务器都具有相同配置文件的副本。
**对于复制模式，至少需要三台服务器，强烈建议您拥有奇数个服务器。 如果您只有两台服务器，那么您处于如果其中一个服务器出现故障，则没有足够的机器来形成大多数法定人数。 两台服务器本身的稳定性比单个服务器稳定，因为有两个单点故障。**

复制模式所需的conf / zoo.cfg文件类似于独立模式下使用的文件，但有一些区别。 这是一个例子：
```
tickTime=2000
dataDir=/var/lib/zookeeper
clientPort=2181
initLimit=5
syncLimit=2
server.1=zoo1:2888:3888
server.2=zoo2:2888:3888
server.3=zoo3:2888:3888
```
initLimit是ZooKeeper用于限制ZooKeeper服务器在仲裁中必须连接到领导者的超时时间长度
syncLimit限制了服务器可以从领导者多远的距离.
使用这两个超时时间，您可以使用tickTime指定时间单位。 在本示例中，initLimit的超时时间为2000毫秒，或10秒钟，为5。

##  Developing Distributed Applications that use ZooKeeper

### The ZooKeeper Data Model

ZNodes

ZooKeeper树中的每个节点都称为znode。 Znodes维护一个统计结构，包括数据更改版本号，acl更改。 统计结构也有时间戳。 版本号与时间戳记一起允许ZooKeeper验证缓存并协调更新。 每次znode的数据发生变化时，版本号都会增加。 例如，每当客户端检索数据时，它也会收到数据的版本。 当客户端执行更新或删除时，它必须提供正在更改的znode的数据版本。 如果它提供的版本与数据的实际版本不匹配，则更新将失败。

znode是程序员需要注意的主要抽象。 Znode有几个特点，值得一提。

- Watch

客户端可以在znode上设置Watch。对znode的更改会触发Watch，然后清除Watch。当手表触发时，ZooKeeper会向客户端发送通知

- 数据访问

存储在命名空间中每个znode处的数据以原子方式读取和写入。读取获取与znode相关联的所有数据字节，写入替换所有数据。
每个节点都有一个访问控制列表（ACL），它限制谁能做什么。

ZooKeeper不是设计为一般数据库或大型对象存储。而是管理协调数据。该数据可以以配置，状态信息，会合等的形式出现。各种形式的协调数据的共同属性是它们相对较小：以千字节为单位。 ZooKeeper客户端和服务器实现具有完整性检查，以确保znode具有少于1M的数据，但数据应远远小于平均值。在相对较大的数据大小上操作将导致一些操作比其他操作花费更多的时间，并且会影响某些操作的延迟，因为通过网络和存储介质移动更多数据所需的额外时间。如果需要大量数据存储，处理此类数据的通常模式是将其存储在大容量存储系统（如NFS或HDFS）上，并将指针存储到ZooKeeper中的存储位置。

- 临时节点

ZooKeeper还具有临时节点的概念。只要创建znode的会话处于活动状态，就会存在这些znodes。当会话结束时，znode被删除。由于这种行为，短暂的znodes不允许有孩子。

- 序列节点 - 唯一命名

在创建znode时，您也可以请求ZooKeeper在路径的末端附加单调增加的计数器。这个计数器对于父znode是唯一的。计数器的格式为％010d - 这是10位数字，0（零）填充（计数器以这种方式进行格式化以简化排序），即“<path> 0000000001”。有关使用此功能的示例，请参阅队列配方。注意：用于存储下一个序列号的计数器是由父节点维护的有符号int（4字节），当计数器超过2147483647（导致名称“<path> -2147483647”）时，计数器将溢出。

ZooKeeper追踪时间多种方式：

-  Zxid

ZooKeeper状态的每次更改都会以zxid（ZooKeeper TransactionId）的形式收到一个戳。
这显示了ZooKeeper的所有更改的总排序。每个更改都将有一个唯一的zxid，如果zxid1小于zxid2，则zxid1发生在zxid2之前。

-     Version numbers
    对节点的每次更改将导致该节点的其中一个版本号的增加。三个版本号是版本（znode的数据更改次数），cversion（znode的子项更改次数）和aversion（znode的ACL更改次数）。

-    Ticks

    当使用多服务器ZooKeeper时，服务器使用ticks来定义事件的定时，例如状态上传，会话超时，对等体之间的连接超时等。tick时间仅通过最小会话超时（2次刻度时间）间接暴露;如果客户端请求超过最小会话超时的会话超时，服务器将告诉客户端会话超时实际上是最小会话超时。

    即时的

    除了在znode创建和znode修改之后将时间戳放入统计结构中，**ZooKeeper不使用实时或时钟时间。**

###  ZooKeeper Stat Structure
ZooKeeper中每个znode的Stat结构由以下字段组成：

-    czxid

     导致此znode被创建的更改的zxid。

-    mzxid

     最后修改此znode的更改的zxid。

-    pzxid

     最后修改znode子项的zxid。

-    ctime

     创建这个znode的时间（以毫秒为单位）。

-   mtime

     当这个znode最后一次修改时，以毫秒为单位的时间。

-     version

     这个znode数据的更改次数。

-    cversion

     这个znode的孩子的更改次数。

-     aversion

     该znode的ACL的更改次数。

-    ephemeralOwner

     如果znode是短暂节点，则该znode的所有者的会话ID。 如果它不是短暂的节点，它将为零。

-    dataLength

     该znode的数据字段的长度。

-    numChildren

     这个znode的孩子的数量。

## ZooKeeper Sessions
 ![](http://zookeeper.apache.org/doc/current/images/state_dia.jpg)
 
 当客户端获取ZooKeeper服务的句柄时，ZooKeeper将创建一个ZooKeeper会话，表示为64位数，它分配给客户端。如果客户端连接到不同的ZooKeeper服务器，它将发送会话ID作为连接握手的一部分。作为安全措施，服务器为任何ZooKeeper服务器可以验证的会话ID创建一个密码。当客户端建立会话时，将密码发送给具有会话ID的客户端。当客户端重新建立与新服务器的会话时，客户端将使用会话ID发送此密码。

ZooKeeper客户端库调用创建ZooKeeper会话的参数之一是会话超时（以毫秒为单位）。客户端发送请求的超时，服务器响应它可以给客户端的超时。当前的实现要求超时时间至少为tickTime（在服务器配置中设置）的2倍，最多为tickTime的20倍。 ZooKeeper客户端API允许访问协商超时。

当客户端（会话）从ZK服务集群分区时，它将开始搜索在会话创建期间指定的服务器列表。最终，当客户端和至少一个服务器之间的连接重新建立时，会话将再次转换到“已连接”状态（如果在会话超时值内重新连接），或者它将转换到“过期”状态（如果会话超时后重新连接）。不建议在断开连接时创建一个新的会话对象（c绑定中的一个新的ZooKeeper.class或zookeeper句柄）。 ZK客户端库将为您处理重新连接。特别是，我们将客户端库中的启发式内置到处理诸如“群体效应”之类的东西...只有在通知会话到期（强制性）时才创建一个新的会话。

会话过期由ZooKeeper集群本身管理，而不是由客户端管理。当ZK客户端与群集建立会话时，会提供上面详述的“超时”值。群集使用此值来确定客户端的会话何时过期。当集群在指定的会话超时时间内没有听到客户端（即没有心跳）时，会发生到期。在会话到期时，集群将删除该会话拥有的任何/所有短暂节点，并立即通知任何/所有连接的客户端更改（任何人观看这些znodes）。此时，过期会话的客户端仍然与集群断开连接，除非能够重新建立与集群的连接，否则不会通知会话到期。客户端将处于断开状态，直到与集群重新建立TCP连接，届时过期会话的观察者将收到“会话到期”通知。