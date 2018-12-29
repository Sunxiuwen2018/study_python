# python基础

### 1. 自我介绍

```python
- 自学能力强
- 不安于现状
- 踏实
- 写成稿子，从接触运维了解python必备工具，兴趣爱好，好玩，python也是大势，开发效率高，库多
顺带解答学python的原因
```

### 2. 为什么学python？和其它语言对比的优势？

```python
2011年毕业，到现在7年了，做了2年的简单运维，在这过程中想向服务器方向发展，和管理服务器的同事了解到除了shell写脚本外还有一门python是必备的，之后查了下发现python无论是代码的简洁度，可读性都非常的明朗，还有看到各大招聘都提到了python这门语言，而且因为喜欢从网上爬自己希望的东西，发现python是里面最简单的，它不像java，c编写那么的繁杂。而且python的第三方库超多，社区也非常活跃，不懂得都可以去查，去问。再则现在现在的人工智能/数据学习/机器学习都以python为第一语言，这是大势，所以想跟着大势走。
```

### 3.  解释型语言和编译型语言区别？

```python
- 编译型语言是将高级代码汇编成机器码，然后生成可执行文件，一次性执行
- 解释型语言是由解释器逐一将代码解释成机器码，一边编译一边执行
```

### 4. py2与py3的区别

```python
1. py2的解释器默认为ASCII,py3的解释器默认为UTF-8
2. py2的str对应py3中的bytes，unicode对应py3中的str
3. py2的类有经典类和新式类，经典类不继承object，py3中的类默认继承object，都是新式类
4. py2中除法/返回int，py3中的除法/返回的是float
5. py2中有yield，py3中有yield，yield from 将可迭代对象转成生成器
6. py2中有range，xarge，py3只有range为可迭代对象
7. print，input，xreadlines
8. py2 有进程池，py3有线程池和进程池
```

### 5. 运算符

```python
- 顺序： () > not > and > or
- or左边非零返回右边的值
- and与or相反
```

### 6. 参数

```python
- 形参：位置、*args、默认、**kwargs
- 实参：位置、默认、混合
- 经典范例
def func(a,b=[]):
    b.append(a)
# 当函数的参数是可变类型数据，其它引用都是调用同一个对象
```

### 7. 装饰器&带参数的装饰器

```python
def counter(num):
    def outer(f):
        def inner(*args,**kwargs):
            rets = []
        	for i in range(num):
                ret = f(*args, **kwargs)
                rets.append(ret)
            return rets
        return inner
    return outer
# 通过带参数实现调用函数的次数
@counter(8)
def f():
    pass
rets =f()
print(rets)          
```

### 8. 生成器

```python
- 本质是迭代器，遵循可迭代协议，不可逆(只能向前不能向后)
yield  类似return，但其不结束函数，下次从该yield后执行
yield from 将可迭代对象转成生成器，也可以是另一个生成器
```

### 9. 列表生成器

```python
v = [lamda :i for i in range(10)]  
v 里存的是函数，但未执行
当v[5]()执行时，此时i为9，故返回值为9
```

### 10. 你用过哪些内置模块？

```python
- os sys time datetime random hashlib re loggin json pickle
- urllib
```

### 11. 用过第三方模块？

```python
requests
bs4  --> from bs4 import Beaufullsoup
pymysql
pymongo
gevent  ?
numpy  ?
panda   ?
```

### 12. 常见的双下划线方法

```python
__new__   
__init__
__call__
__dict__
__doc__
__name__
__base__

__getattr__
__setattr__
__delattr__

__getitem__
__setitem__
__delitem__

__str__
__repr__
__enter__
__exit__
```

### 13. 什么是单利模式？

```python
某个类只能出现一个实例
```

### 14. 哪里用到单利模式

```python
1. 模块的导入就是单利模式
只有第一次导入时加载生成pyc文件，后面加载只会加载一次，如django的admin注册admin.site
2. 数据库连接池
```

### 15. 如何写单利模式？

```python
- 通过类
import threading
Class Single(object):
    _instance = None
    _clock = threading.Rlock()
    
    def __new__(cls,*args,**kwargs):
        if cls._instance:
            return cls._instane
        with cls._clock:  # 应对多线程
            if not cls._instance:
                cls._instance = objece.__new__(*args,**kwargs)
                return cls._instance
```

### 16. OSI七层模型

```python
物理层、数据链数层、网络层、传输层、会话层、表示层、应用层
2：arp协议通过ip找mac
3：ip协议
7：http、ftp、smtp、pop3、imap
socket 是应用层和传输层之间的抽象层
```

### 17. tcp三次握手

```
1. 客户端向服务端发送请求连接
2. 服务端回复客户端两个标识，一个syn表示已接到请求，一个ack表示服务端已在做连接的准备
3. 客户端收到服务端的回复后，客户端准备连接的所有资源，发送一个ack，表示客户端准备工作已完成，两者进入连接。
之所以3次，是因为第三次要保证服务器发送的ack被客户端接收到了，才行

体现：服务端accept，客户端conect
```

### 18. tcp四次挥手

```python
1. 连接双方其中的a向b发送断开请求
2. b收到后回复a，收到请求，开始准备断开资源
3. b准备完成后，再次向a发送，没有要传的数据了，可以断开了
4. a收到b回复后，准备断开连接，回收资源，回复b确认断开连接，等待2mls后，a断开连接

体现：close()
```

### 19. tcp和udp的区别

```python
tcp 是面向数据流，面向连接的请求，每次请求都需要得到回复才行所以是安全的
udp 是面向包，无连接，它的传输效率高，但不安全，常见的视频，语音
```

### 20. 粘包及如何解决

```python
数据传输双方都是基于缓存区传输的，当数据量很小，间隔很短时，会等一会，进行合包，当一个包发送，
再则接收方来不及时接收缓冲区的包，造成多个包接收，从而造成粘包
本质是接收方不知道消息之间的界限，不知道一次提取多少字节的数据造成的。
在发送数据前，把自己要发送的字节流总大小告诉接收端，如何接收端循环接收完所有数据。
python中使用struck模块，将数据转成固定长度的bytes类型，服务端通过struck模块接收
heard = struck.pack('i', 'dddd') 4个字节
struck.unpack('i' header)
```

### 21.  什么是cdn

```python
内容分发，公司主要租cdn讲js，css等文件存在各地，当用户获取时就进获取，提高体验。
```

### 22. 手写socket

```python
---tcp
import socket
-server
sk = socket.socket()
sk.bind((ip, port))
sk.lister()
conn, addr = sk.accept()
data = conn.recv(size)
conn.send('xxxx'.encoding('utf-8'))
conn.close()
sk.close()

-client
sk = socket.socket()
sk.connect((ip,port))
sk.send(data.encode('utf-8'))
res = sk.recv(1024).decode('utf-8')
sk.close()

--udp
sk = socket.socket(type=socket.SOCK_DGRAM)
sk.bind((ip,port))
data,add = sk.recvfrom(1024)
sk.sendto(msg,add)
sk.close()

sk = socket.socket(type=socket.SOCK_DGRAM)
sk.sendto(msg,(ip,port))
data,add = sk.recvfrom(1024)
sk.close()
```

### 23. 进程/线程/协程的区别？

```python
- 进程：计算机资源分配的最小单元
- 线程：cpu调度的最小单位
- 协程：单线程实现并发，本质是单线程下，由用户自己控制任务遇到io阻塞就切换另一个任务去执行，提升效率。
io密集型才用多线程，计算密集型采用多进程
进程间资源不共享，线程间资源共享
线程的开销比进程小
多线程一定是在一个进程里开启的
线程启动的速度快
```

### 24. GIL锁

```python
GIL锁是全局解释器锁，基于Cpython实现，实现同一时刻，python解释器只能运行一个线程的代码。
GIL锁保护解释器级别的数据如垃圾回收的数据，LOCK锁是保护应用程序的数据
GIL锁的存在，导致多线程无法利用多核，它也没有办法保证数据的安全，因为它只是锁一个进程中的线程，另一个进程中的线程是可以同时访问共享数据的，从而不安全。
```

### 25. 进程之间如何进行通信？

```python
通过mutiprocessing中提供的队列和管道，都是将数据存放于内存中，可以使进程间通信
队列是基于管道+锁实现的
- 信号量：资源有限，同时允许一定数量的进程访问修改数据，一把锁对应多把钥匙，锁 + 计数器
	多少个任务开多少个进程
- 进程池是开启固定数量的进程，干多个任务，一次干的任务数受限于进程池中进程的数量
```

### 26. 进程间是如何资源共享的？

```python
python是通过一个Manger模块来实现的
```

### 27. 线程和进程的基本使用：方法和参数

```python
- 创建子进程【本身是异步运行】
from mutiprocessing import Process,Lock
def f(v):
    print(v)
if __name__ == '__main__':
    p = Process(target=f,args=('go', ))
    p.start() # 调用操作系统命令创建子进程
    p.join()  # 主进程等待子进程p运行结束后才运行，阻塞
    print('主进程进场了')
- 同步需要加锁
lock = Lock()  # 互斥锁
lock.acquire() # 获取
lock.release() # 归还
```

### 27. 线程池和进程池

```python
- 减少开闭进程线程池的开销
- 保证同一时间最多有固定数量的进程
from multiprocessing import Pool
p = Pool(num)
p.apply(func,args=(i,))  # 同步
p.apply_async(func,args=(j,)) # 异步
p.close()
p.join()
```

### 28. IO多路复用

```python
IO模型，遇到io就切换
同步调用：一个进程在执行某个任务时，另一个进程必须等待其完成后，才能执行
异步调用：一个进程执行多个任务，不需要等待这个进程结束就去执行下一个进程
阻塞：是指调用结果返回之前，当前线程/进程会被挂起，只有在得到结果之后才会将阻塞的线程/进程激活
非阻塞：指在不能立刻得到结果之前也立刻返回，同时该函数不会阻塞当前线程
阻塞IO：就是在IO执行的两个阶段(等待和拷贝数据)都被阻塞了
IO多路复用：
- 监听多个“socket” 是否发生变化(收/发数据)
三种：
select 最多监听1024个socket对象，内部基于轮询检测
poll，无socket个数限制，内部同样基于轮询检测
epoll，无socket个数限制，内部socket有变化通过回调函数监听，自动举手
epoll只支持Linux
```

### 29. 什么是并行和并发？

```python
- 并行：发生在多核，同一时刻，执行多个任务
- 并发：发生在单核，同一段时间，执行多个任务，宏观看一样，实际是轮询
```

### 30. 哪里用到反射？

```python
django 的setting配置，cbv编程路由匹配，中间件
```

### 31. 谈谈对面向对象的认识？

```python
封装: 将一个对象的数据集合在一个对象中. 方便使用和调取
继承: 在已知的类的基础上进一步对类进行扩展. 减少冗余代码的开发
多态: python天生多态，变量动态绑定，一个对象站在不同的角度它有多种形态。
```

### 32. 可迭代对象

```python
有__iter__ 方法，返回可迭代对象
def __iter__(self):
    return iter([11,22,33])
```

### 33. 互斥锁、递归锁、GIL锁

```python
互斥锁是解决多线程数据共享保证安全的，只能一次申请一次释放
递归锁是解决互斥锁导致的死锁，而出生的，一个线程可以多次获取锁和释放锁
GIL锁是cpython特有的全局解释器锁，保证同一时刻，一个进程中的多线程只能一个线程被cpu调度，不能保证数据安全
```

### 34. 什么是反射，在哪里用到？

```python
- 反射，通过字符串的形式操作对象的属性，可以判断，查询，设置，删除
在django的CBV编写视图的路由系统中的dispach方法就是根据反射来实现不同的请求执行不同的方法
像setting中的配置，中间件，导入模块都是通过反射来的
```

### 35. json 支持哪些数据类型

```python
除set外，python的其它数据类型都支持，不支持datetime，django中的Jsonresponse支持时间类型
```



# 数据库

### 1.  你了解的数据库引擎及区别

```python
inodb   支持事务，表锁，行锁(主键)
mysiam  不支持事务，表锁，一查全表锁，不好
```

### 2. 事务

```python
多个sql语句打包一起，要么全部执行，要么全部不执行
原生操作：
begin；
select * from tb for update;
commit;
特点：
原子性：要么全成，要么全败
一致性：如ab，a变了多少，b也要跟着变
隔离性：不同的事务间互不干扰
持久性：一旦成功就会写入硬盘
```

### 3. 索引的作用以及种类？

```python
- 作用
1. 加速查找   因为其内部结构是b+树，可以快速查找，不用遍历所有的表数据
2. 约束 【唯一索引】
- 种类
主键索引：加速；不能为空，不能重复
唯一索引：加速；不能重复
普通索引:加速
联合索引：多个字段，加速
联合唯一索引：加速；联合唯一
注：联合索引时候，如果想要命中索引必须遵循“最左前缀原则”
命中：(user,pwd,age)
都要包括最左边的字段索引
无法命中：
pwd
age
pwd,age

覆盖索引，在索引的数据结构中就可以找到想要的数据
索引合并，使用多个单列索引进行查询
```

### 4. mysql优化

```python
分库，大库分成多个小库
分表
水平分表   将不用的列分到其它表
垂直分表   比如将3年前的数据分到其它的表
读写分离
数据存放在内存   如男女等常用数据，放在内存中
命中索引
缓存     放到redis等中
确定要一个数据时，用limit，不要它查到了还去查表
```

### 5. char和varchar的区别

### 6. redis和memcached

```python
- 相同点:都是在内存保存.
    - 不同点:
        数据类型:
            redis有5种数据类型
                redis={
                    'k1':12, 字符串
                    'k2':[11,22,33,22], 列表
                    'k3':{'name':xx,age:11}, 字典
                    'k4':{11,22,33}, 集合
                    'k5':{('alex',10),('oldboy',90),('eric',60)}, 有序集合
                }
            memcached只有1中数据类型
                memcached = {
                    'k1':'123'
                }
        持久化:
            - redis,支持
            - memcached,不支持.
```

### 7.redis的持久化

```python
- 在配置文件中
AOF  : 将执行过的所有redis命令保存起来
ROB: 固定间隔时间进行持久化
```

### 8. 持久化

### 9. 哨兵

### 10. 分布式集群

### redis数据过期策略

root/106.13.38.227

z961125@









