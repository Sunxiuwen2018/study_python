# python小结
## 一、基础数据类型概括 
```python
1. 布尔 bool =>真假
2. 数字 int
3. 浮点型 float
4. 空   None   ==> 空不是假，不能直接用于条件判断，需要加not/is才行，如 not None 或 is None
5. 字符串 str
6. 列表 list
7. 元组 tuple  ==> 不可变的列表，序列化会和列表一样的效果，区别是反序列化回来不会变成元组，而是列表
8. 字典 dict
9. 集合 set

**总结**
    1. 可迭代数据类型：str、list、tuple、dict、set
    2. 不可变数据类型：bool、int、float、str、tuple
    3. 可变数据类型：list、dict、set
    4. 可通过`+`号数据类型：int、float、str、list、tuple

    # 列表，字典，集合都有pop方法，del方法
    # pop 列表按索引，字典按对象，集合随机删
    # del 列表按索引，字典，集合按对象，只能删除整个集合
    # remove 列表按对象，集合按对象，没有都报错，字典没有该方法,
    # 列表批量增加extend，字典/集合update
```

### 布尔bool
```python
1. 非0,非空则为True，None不是False[通过is或==判断都是不正确的]，只有None,0,"",[],(),{},ser()等通过bool转化才为False
2. is 判断的是内存地址，== 判断的是值
3. 条件判断优先级顺序： 括号，not, and, or
4. 对于or，左边非零取左边，and相反
```

### 整形int
```python
**基础**
    二进制： 0，1
    八进制： 0~7     三位一体
    十进制： 0~9
    十六进制： 0~F   四位一体
```

**进制转换**

```python
进制之间的转换要注意每个进制的基本数码范围！！！

二：0b  八：0o  十六：0x

二进制转十进制   int('1110', 2)     # 后面的2就表示2进制
八进制转十进制   int('12345670', 8)
十六进制转十进制 int('9ABCDEF', 16)

十进制转二进制   bin(100)
十进制转成八进制  oct(8)
十进制转十六进制  hex(10)
二进制转十六进制  hex(int('111',2))
```

**方法**

```python
int.bit_length()   转化成二进制后的位数
    py2与py3除法区别
    py3:
        3 / 2  ==> 1.5   整除得float
    py2：
        3 / 2  ==> 1     整除得int，除非除数或被除数为float才得float
        3.0 /2 ==>1.5
    py2与py3 整除(//)，取模 结果相同
```

### 字符串
    **基础**
    **不可变，可切片取值，可迭代**
    分割拼接替换处理：
    str.strip("char")   默认清除左右的空格，空白字符，也可指定左右的某个字符清理
    str.replace(old,new,count)  替换字符，可指定次数
    str.split("char"，count)    以char进行分割，可指定次数，将字符串转换成列表
    "".join(str(i) for i in [11,22,33])  将可迭代的列表等转换成字符串，注意字符串拼接必须是str，int不行，需要先转才行
    
    格式化：
    "%s_%d_%.2f" %('china', 22, 2)  格式化
    "%(name)s_%(age)d" %({"name":'china', "age":30})   可用字典
    "{0}_{1}_{0}".format(a,b)
    "{user}_{pwd}".format(**{'user':'bei','pwd':30})
    f"{name}"
    
    字母的处理：
    str.captalize()   首字母大写，其它都小写
    str.swapcase()  大小写反转
    stt.title()     单词间空白或以下划线分割的字母首字母大写，其它字母都小写
    str.upper()     单词全部转成大写
    str.isupper()
    str.lower()
    str.islower()
    str.satrswith('char')   以什么开头
    str.endswith()
    str.isspace()     注意空字符串不是全部空白，需要中间加空格才行如：" "
    
    查找元素：
    str.index('char', start,end)   查找元素的索引，有多个，发回第一次找到的元素的索引，没有报错
    str.find('char', start,end)    查索引，没有返回-1


### 列表list
    **基础**
        可变，可切片,可迭代,list的pop，del增删靠索引，字典靠元素
    **增**
        list.append(object)  无返回值，添加到最后
        list.insert(index,object) 无返回值，按索引添加
        list.extend(iterable)  无返回值，添加可迭代数据类型到最后，不会去重，支持的数据类型有==>列表，元组,字符串,字典的key,集合
    **删**
        list.pop(index=None)  返回值为删除的元素，默认删除最后一个元素，也可以删除指定索引的元素
        list.remove(object)   无返回值，删除指定元素
        del list[index]       无返回值，删除指定索引的元素
        del list              无返回值，删除列表
        list.clear()          无返回值，清空列表，列表还在
    **改**
        list[index]=newdata       按索引改
        list[:index]=[newdata]    按切片改，改的是整个连续的内存块，左右的元素个数可以不一样且都必须是可迭代的，（一旦切片有步长，就必须元素个数一致才行）！！！
    **查**
        list[index:]    按索引或切片查
        list.index(object,start=None,end=None)   查询某个元素的索引，没有报错,或者指定范围内第一次出现改元素的索引，注意范围取值为[start,end)
        [(index,object) for i in enumerate(list,start=1)]  按循环查
    **other**
        list.count(obj)  某个元素出现的次数
        len(list)        列表的长度  调用__len__
        list.sort(revers=False)   改变了列表，直接改变列表中元素排序，默认升序，revers为True时降序
        list.revers()    改变了列表，直接将列表中元素顺序反转过来，不排序
        list.copy()      浅拷贝
        sorted(list)     可以完整拷贝，生成新的列表，里面也可以通过function来定义数据排序等
        object in list   成员判断

### 元组tuple
```python
**不可变，只读列表，有序，可迭代，元素可以为任意数据类型**
**方法**
    tu.index(obj, start,end)
    tu.count(obj)
    len(tu)
**注意点**
    单个元素时，要在后面加逗号： tu =(11,)   不加逗号就不是元组了，而是int
    i = 1,    这个也是元组
# 涉及到数据共享时，必须用不可变的数据类型，如DRF框架中版本组件返回值就是一个版本号和版本实例化对象，django的路由系统也是返回一个三元组
```

### 字典dict
    dic = {}
    key 与 value 的映射关系
    key为可哈希的，即不可变数据类型，int，bool，float，str，tuple
    value可为任意类型，即list，dict，set
    **增：**
    dic[key] = value1    本质调用__getitem__和__setitem__
    dic1.update(dic2)   将dic2中的内容导入dic1，如果与dic1中key相同则覆盖更新
    dic.setdefault(key,value)  value默认为None，一旦创建就无法更改，value为可变数据类型【】，可向里面添加，共用一个内存空间
    dict.fromkeys([a,b],value)  ==> {a:value,b:value}, value如果是可变数据类型，那么同上面一样也可添加，静态方法==>类和对象都可以调用，它没有self或cls参数，和普通函数一样
    **删：**
    dic.pop(key)   返回删除的值
    del dic[key]   无返回值
    del dic        从内存中删除dic
    dic.clear()    清空列表
    dic.popitem()  随机删除一个
    **改：**
    dic[newkey] = value
    dic.update(dic2)
    **查：**
    dic[key]      没有报错
    dic.get(key)  没有返回None
    dic.values()
    dic.keys()
    dic.items()

### 集合set
```python
**基础**
    `可变数据类型`，`无序`，可增，删，不能直接改，`不能切片`，`元素唯一`，且只能是`不可哈希`类型

**增**
set.add(obj)
set.update(iterable)  打散元素添加到集合中
**删**
set.pop()  随机删除一个
set.remove(obj)
set.clear()
del set
**查**
没有方法用，无序不能切片，只能循环匹配
**共用**
len(set)
set.copy() 浅拷贝
```

## 文件操作

### 基本操作

```python
- 打开文件本质调用两个方法,python上下文管理
__enter__ 和 __exit__

f = open(filepath, method, encoding='utf-8')
f.read()
f.readline() # 读取一行
f.readlines() # 一行行全部读出，放在列表中
f.close()
```

## 面试考点

### py2与py3的区别

```python
1. py2解释器的默认编码为ASCII码，py3解释器默认编码为utf-8
2. py2中的str对应py3中的bytes，unicode对应py3中的str
3. py2中的类有经典类和新式类，py3中只有新式类，默认继承object类
4. py2中只有yield，py3中除了yield还有yield from 可以把一个可迭代对象转成生成器
5. py2的int相除返回为int，py3为float
6. py2的print可括号也可以引号，2.6后可括号可不括号，py3需要括号
7. py2有input输入int返回int型和raw_input输入int返回str型，py3中只有input，返回都为str型
8. py2有xrange生成器和range，py3只有range，他为可迭代对象
9. py2文件操作有xreadlines它为生成器，py3没有
10. py2 有进程池，py3有线程池和进程池
```

### Ascii,Unicode,Utf-8，Gbk的区别

```python
ASCII码为计算机最原始的编码，127个，因为是美国人发明的，没有中文，一个字符占一个字节
Unicode为万国码，包含了所有国家的编码，一个字节占4个字节
Utf-8为可变长度编码，对英文，数字还是一个字符占一个字节，对中文是一个中文占3个字节
GBK为国标码，是因为万国码太占空间了，一个字符占3个字节
```

### UTF-8与GBK及unicode之间的转换

```python
utf8不能直接转gbk除了英文数字，都需要通过unicode中转
1. utf-8 --> gbk
s.decode('utf-8').encode('gbk')  # 先通过decode将utf8转成unicode，再通过encode将unicode编码成gbk
```

### python的安装方式

```python
- pip包管理安装
1. pip intall package
- 源码安装
1. 下载，解压，切换到解码目录
2. 编译：python setup.py build
3. 安装：python setup.py install
```

### python的深浅拷贝

```python
- 浅拷贝：如果有嵌套的话，拷贝的是对象的第一层，改边嵌套层数据，拷贝与被拷贝方都会改变
- 深拷贝：拷贝所有层 import copy  a = copy.deepcopy(li)
```

### python的垃圾回收机制

```python
- 计数   计算变量被引用的次数，引用则+，引用对象删除则-
- 标记&清除 当内存不够时，遍历所有对象，看对象是否被引用，有则标记，遍历一遍后，把没有标记的删除
- 分代  多次遍历，都存活的进行分代，提升层级，层级越高存活越久

python的GC模块主要运用了引用计数的方法来跟踪和回收垃圾，但无法解决两个对象循环引用的问题，所以在此基础上通过标记-清除解决容器对象可能的循环引用，通过分代回收以空间换时间来进一步提高垃圾回收的效率。
```

###  解释型语言和编译型语言区别？

```pyton
编译型：运行前先由编译器将高级语言代码编译为对应机器的cpu汇编指令集，再由汇编器汇编为目标机器码，生成可执行文件，然最后运行生成的可执行文件。最典型的代表语言为C/C++，一般生成的可执行文件及.exe文件。 

解释型：在运行时由翻译器将高级语言代码翻译成易于执行的中间代码，并由解释器（例如浏览器、虚拟机）逐一将该中间代码解释成机器码并执行（可看做是将编译、运行合二为一了）。最典型的代表语言为JavaScript、Python、Ruby和Perl等。 
```

# 二、函数

## 函数名

```python
- 函数名就是一个变量
1. 查看函数名：func_name.__name__
2. 查看装饰器后的函数名
from functools import warps
def wra(f):
    @warps
    def inner()
    ……
```

## 函数参数

```python
- 函数声明的位置写的变量的声明
- *args：接收多余的位置参数，以元组的方式呈现
- **kwargs:接收多余的关键字参数，以字典的方式呈现
- 形参顺序：位置参数、*args、默认参数、**kwargs
- 经典范例
def func(a,b=[]):
    b.append(a)
# 当函数的参数是可变类型数据，其它引用都是调用同一个对象
```

## 闭包

```python
- 特点：
1. 让一个变量常驻内存，不会随着函数的结束而关闭，减少开闭内存空间，提升执行效率
2. 可以保护变量不被侵占修改
- 应用
1. 装饰器就是一个闭包
```

## 三大器之装饰器

- 定义：在不改变原函数的源代码和调用方式外，添加额外的功能，动态代理

- 基本实例

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

- 多层装饰器执行顺序

  ```python
  ([func])
  ```

- 应用

  ```python
  - flask路由系统就是通过装饰器
  ```

## 三大器之迭代器

```python
- 可迭代对象：内部含有__iter__方法
	print('__iter__' in dir(list))
- 迭代器：内部含有__iter__和__next__方法
	print('__iter__' and '__next__' in dir(obj))   # 判断对象是否有该两个方法
	form collections import Iterator,Iterable
    print(isinstance(obj, Iterable))
- 可迭代对象转迭代器
	obj.__iter__()
- 迭代器取值
	obj.__next__()
- 好处
1. 节省内存
2. 满足惰性机制，一次只取一个次
3. 从前到后，不可逆
- 哪些使用了
1. for、sum、Max、min、生成器
- 小缺点
当取完值时，再取会报StopIteration,所以每次都通过try来解决
```

## 三大器之生成器

```python
- 本质：迭代器，遵循迭代器的规则
- 可以模拟阻塞，异步，python中的携程实现就是通过生成器来实现任务之间的切换
- 特点：执行这个函数，并没有运行，而是帮你创建一个生成器对象，【生成器中对象中存的时代码！！！】
- 创建
1. 生成器函数
def ge():
    yield xxx
gn = ge()
gn.__next__()  或者用for
send() 为上一个yield的位置传值，在下一次调用函数时会返回

yield from 可迭代对象  : 将可迭代对象转成生成器

2. 生成器表达式
gn = (i for i in range(20))

3. 推导式
[i for i in range(10) if i >2]
{k:v for k,v in enumerate(li, 1) if}
{key for 循环 if }
4. 三元表达式
v1 if 条件 else v2    # 条件为真时取v1
5. 扩展
js： 条件？v1:v2
    
- 进阶
v = [lamda :i for i in range(10)]  
v 里存的是函数，但未执行
当v[5]()执行时，此时i为9，故返回值为9
```

## 内置函数

```python
- 作用域
globals()
locals()
- bin(),oct(),hex(),int()
- ord(c) c对应的ASCII码值，chr(3) 对应的字符
- divmod(a,b)  => 返回(商，余数)  ==> 用着分页
- round(33.222, 2)  => 四舍五入，保留2位小数
- len()
- enumerate(list,start=int)  解构=> index,obj

- reversed(序列)  => 生成新的对象，返回迭代器，反转
- sorted(iter,key) =>排序
- max(iter,key=func) => max(list,key=lambda x:x*-1)
- min(同上)
- filter(func,iterble)  # 过滤，指定的值
- map(func,iterble)  # 循环迭代对象的每个元素，调用函数，返回列表
- zip(iter,iter) ==>拉链  list(zip([1,2],[2,3])) = > [[1,2],[2,3]]
- reduce() 
from functools import reduce  # 归纳
li = [1,2,5,6]  # 先算前两位之和，之后和后面的数相加
s = reduce(lambda x,y:x+y, li)  => 1,2:1+2 => 3,5 =>3+5 =>8,6 => 14

- eval()  ==> 执行字符串表达式的值，有返回值  eval('round(33.3333,2)') =>33.33
- exec()  ==> 同样执行字符串的表达式，可以执行更复杂的命令，返回值为None
```

# 三、面向对象

### 编程模式

- 面向过程：按照事务的发展顺序去写代码，局限性大，非常复杂的项目就不好处理
- 面向对象：侧重点在对象，让对象去做指定事情，所有的数据都保存在对象里面，扩展性强，以对象为中心

### 面向对象三大特性

```python
- 封装 ：隐藏对象的属性和实现细节，便于将变化隔离，提高复用性，安全性，提供统一的接口
	1. 组合：给一个类的对象，封装一个属性，这个属性是另一个类的对象
- 继承：子类可以自动拥有父类中除了私有内容(即双下划线开头定义的方法和属性)外的其它所有内容
	1. python中支持多继承，java等中不支持
    2. py3中类继承mro的核心是C3算法
- 多态：python天生多态，python的对象没有指定数据类型，执行的是动态数据绑定
	同一个对象，拥有多种形态，python的多态性经典的就是鸭子模型，看起来像就是，如list，dict，set都有pop方法
    
from abc import ABCMeta，abstractmethod
# 抽象类中可以有抽象方法
# 有抽象方法的类一定是抽象类
# 接口类：类中所有的方法都是抽象方法
class Base(metaclass=ABCMeta):
    @abstractmethod
    def login(self):
        pass   # 对子类进行约束，约束子类中必须要重写该方法，否则报错
- 约束
	父类对子类进行约束
    1. 使用抛异常的形式来完成对子类的约束
    2. 使用抽象类，接口类来完成约束
```

```python
- 备注C3算法算继承
class A:
    pass
class B(A):
    pass
class C(A):
    pass
class D(B,C):
    pass
class E(D, A):
    pass
class F(D):
    pass
class G(E):
    pass
class H:
    pass

class I(H, F, G):
    pass
print(I.__mro__)
'''
    设L()为求某个类的MRO
    1. 拆分
    L(I) = I + L(H) + L(F) + L(G) + HFG
    L(H) = H 
    L(F) = F + L(D) + D
    L(G) = G + L(E) + E
    L(D) = D + L(B) + L(C) + BC
    L(E) = E + L(D) + L(A) + DA
    L(A) = A
    L(B) = B + L(A) + A
    L(C) = C + L(A) + A
    
    2. 合并, c3算法的核心就是这个merge, 用前面的第一项的头和后面每一项的身体比较. 如果头没有在后面的身体里出现. 
    这个头会被算出, 继续用头去比较后面的身体. 如果头在后面的身体中出现了, 此时更换为第二项的头继续和其他项的身体比较
    .....
    
    L(I) = IHFGEDBCA
    L(H) = H 
    L(F) = FDBCA
    L(G) = GEDBCA
    L(D) = DBCA
    L(E) = EDBCA
    L(A) = A
    L(B) = BA
    L(C) = CA
'''
```

### self是谁

```python
谁调用的就是谁
```

### super的作用

```python
根据mro的顺序，执行下一个类中对应的方法
#如继承顺序是：A-B-C-D
super().方法（）# 执行当前对象的下一个类中对应的方法，即父类A
super(B,self).方法() # 即找B类的下一个继承C中的方法
```

### 单例模式

> 某个类只有一个实例
>
> 最常见的就是模块导入就是一个单例模式，一个模块导入解释器只会载入一次

1. 通过__new__建立单利模式

```python
# 要考虑多线程，当创建对象时很慢，那么就不是单利了，所以要加上锁
import threading
class SingleInstance(object):
    """单例模式"""
    _instance = None
	_lock = threading.Rlock()
    
    def __new__(cls, *args, **kwargs):
        if cls._instance:
            return cls._instance
        with cls._lock:
            if cls._instance is None:
                cls._instance = super().__new__(cls, *args, **kwargs)
            return cls._instance


class Me(object):
    """解决计算实例化了多少个实例"""
    _count = 0

    def __new__(cls, *args, **kwargs):
        cls._count += 1
        super().__new__(cls)
        
class Wo:
    _count = 0
    def __init__(self,name):
        Wo._count +=1
        self.name = name
print(Wo._count)
```

### 哪里用到单利模式？

```python
1. 模块的导入就是单利模式
只有第一次导入时加载生成pyc文件，后面加载只会加载一次，如django的admin注册admin.site
2. 数据库连接池
```

### 类方法、静态方法、实例方法、特性

```python
- 类方法 @classmethod  通常给类使用，第一个参数必须是cls，本质是类中定义的方法
	任何情况都是方法
- 静态方法 @staticmethod 对参数没有要求，本质是在类中声明了一堆函数,都能调用
    cls.fun() 
    任何情况都是函数
- 实例方法
	1. 类名.方法()  此时方法就是函数
    2. 对象.方法()   此时就是方法
	1. 绑定给对象用的方法，如__init__，类中所有的函数，都是对象的绑定方法
    obj.fun()
- 特性 @property
	1. 没有参数，将方法当属性使用,不能被赋值
__开头的内容，只能是类中调用，对象和子类无法调用，本质是变形：_类名__xxx

-- 类方法和静态方法的区别
相同点：
1. 都可以用类名去调用里面的方法和属性
2. 不需要实例化
不同点：
1. 静态方法不需要传self
2. 类方法必须有一个cls参数表示这个类，可以使用类属性
```

### 特殊方法

```python
__new__  返回一个对象
__init__ 构造方法，为对象封装属性
__call__ 对象加括号，flask的app.run()就是这个的调用，django的wsgi也是
__enter__ with管理文件的打开
__exit__  文件的关闭
__str__   打印对象的显示
__repr__ 对象的官方字符串表示，很多时候容器类打印  repr() 把一个对象还原成应该显示的样子
__getattr__ 反射中的获取对象的属性
__setattr__
__delattr__
__hasattr__
__getitem__  obj[key]  对象中括号获取属性
__setitem__
__delitem__
__del__ 析构方法
__doc__
__name__
__dict__ 对象或类中的所有的属性或方法
__base__ 类的所有父类

```

#  四、网络

```python
- osi七层模型
- 三次握手
- 四次挥手
- tcp、udp区别：
tcp  流  
udp  包   不安全不保证安全到达，速度快
```

### 进程、线程、携程

```python
进程是计算机中最小的资源分配单位
线程cpu调度的最小单位
协程  是由程序员创建的，可以称为微线程，来回切换，不一定提高效率，当有IO时切换，那么效率就高些，让线程不闲置，它就是一个线程，通过切换来执行的
```

# 五、算法

- 冒泡

  ```python
  # 循环模式
  # 核心：从头开始比较相邻两个数的大小，然后大的数与小的数交换位置，一直到最后一个，然后循环
  for i in range(len(list) -1 ):  # 列表中多少个数，就比较多少趟,最后一次不用比
      flag = False   # 设定条件，当循环一遍没有改变时，表示已经排好序了，修改flag，然后直接退出
      for j in range(len(list) - i - 1)：  # 选一个数还要和列表中剩下的所有数比一次
      	if list[j] > list[j+1]:
              list[j], list[j+1] = list[j+1], list[j]
              flag = True
      if not flag:
          break  
  ```

- 二分查找

  ```python
  # 前提列表必须是有序的
  # 核心：掐头结尾取中间
  def two_search(li, value):
  	left = 0
      right = len(li) -1 # 右边的索引
      mind = (left + right) // 2
      while left <= right:
          if li[mind] == value:
              return f'{value} index is: {mind}'
          elif li[mind] > value:  # 说明要找的值在左边，首索引不变，尾索引移到mind前面
              right = mind -1
          elif li[mind] < value:
              left = mind + 1
      else:
          print(f'列表中不存在{value}')      
  ```

- 通过列表模拟栈

  ```python
  class Stack:
      def __init__(self, size):
          self.size = size  # 指定栈的大小  ，len(list)
          self.lst = []
          self.index = 0  # 栈顶，也就是就下面的位置,时刻为下一个数的索引，开始为空，即为0
      def push(self,v):
          if self.index >= size：
          	raise Exception('栈满了')
          self.lst.insert(self.index, v)
          self.index += 1
     def pop(self,v):
      	if self.index <=0:
              raise Exception('栈空了')
     		self.index -=1  # 从上往下去，最开始index在外面
          return self.lst[self.index]
          
  ```

- 

- 

- 树 - 》堆

- 红黑树

- 索引的本质，B树，B+树


```
python学习工具
公众号：菜鸟学python
书：a byte of python，简明python教程，父与子的变成之旅，笨办法学python
视频：网易云课堂
网站：廖雪峰的官方网站，菜鸟教程，
工具：sublime，pycharm，visual studio

后端工程师技能要求：
1、前端要求：熟悉html+css+js+jquery
2、三大框架：vue，bootstrap，react，angular

网络编程需要背诵：
1、tcp/udp套接字连接模型
2、lock，锁，同步控制，《买票》
3、队列，queue，同步控制《生产者消费者模型》
4、进程池之回调函数
5、多进程，多线程（线程池），协程解原生socket弊端
6、IO多路复用

ps：线程池回调函数是在子线程运行
    进程池回调函数是在主进程运行

http请求8种方法： get，post，head，delete，put，options，connect，trace

post与get的区别？
1、get提交的数据会放在url之后，以？分割，并以键值的形式进行拼接，多个键值以&拼接，post请求数据是放在请求体中，get没有请求体
2、get提交的数据长度有限制（不同浏览器对url的长度有限制），post对数据的长度没有限制
3、get通过request.querystring获取变量值，post通过request.form来获取
4、get提交数据不安全，全部以明码方式显示在url上，post没有

输入url后发生的事情？
1、浏览器向dns申请解析域名所对应的ip
2、获取ip后，浏览器根据ip及端口号，向服务器发起tcp三次握手，建立连接
3、浏览器向服务器发起http请求
4、服务器根据请求中的参数做出响应，并将对应的资源发送给浏览器
5、浏览器拿到数据对页面进行渲染，显示内容
6、释放tcp连接，四次挥手

请求格式：
请求行：请求方法 http协议  版本
请求头：键值模式
空行
请求体：get请求没有，还是key=value



django框架拾遗
1、如果app未注册，那么做数据迁移就会报错
  注册格式： 应用名.apps.驼峰格式应用名Confing


2、静态文件目录，不管多少个目录，统一别名还用static

3、input标签加上required则必填，取消前端校验，在form标签上加上novalid

4、orm建好表后，再增加字段，需清空数据，不然报错，或者设置默认值

5、print先调用__str__，再repr，repr是容器类数据类型使用
   __str__=__repr__ 则结果一样



前端：

1.overflow：handle   和clear:both 区别，都在什么情况下使用其清除浮动？

2.选项卡，排他思想不理解？for循环点击事件？

3、inline-block 两个行内块中间会有空白折叠现象，可将父盒子font-size= 0 解决
使用 display:inline-block; 能解决元素在一行的问题，但是会存在行内元素在一行显示的问题：

div 之间的空格问题，可由父盒子的 font-size:0; 解决
div 垂直方向上的对齐问题，可由 vertical-align: base; 解决


/*设置绝对定位之后，margin:0 auto;不起任何作用，如果想让绝对定位的盒子居中。
当做公式记下来 设置子元素绝对定位，然后left:50%;
margin-left等于元素宽度的一半，实现绝对定位盒子居中*/


4、什么时候用css，什么时候用attr


list.remove()
set.remove()


python模块：
    日志模块：
        一、两种模式
            1.1、模块级默认配置函数（一般模式）
            特点：
                a、手动设置位置，手动设置信息
                b、无法同时标准输出到控制台和记录文件
                c、可以总体设置格式，无法单独某个，无法分割信息到不同文件及个性化格式设置
            1.2、流程
                1、导入模块  import logging
                2、选好程序位置，设置格式（可以配置多个参数）
                logging.basicConfig(
                                level=logging.DEBUG,
                                format ='%(asctime)s-%(filename)s-%(messages)s',
                                filename = 'my_log.log')
                3、设置日志记录信息
                    logging.DEBUG('debug:message')
                    logging.INFO('info:message')
                    logging.WARNING('waring:message')
                    logging.ERROR('error:message')
                    logging.critical('critical:message')
                注：message是字符串所以可以格式化%传变量
            2.1、自定义版，通过logging四大组件配置
            特点：
                1、可同时屏幕，文件写入
                2、可设全局日志级别，日记文件写入级别，屏幕打印级别及三个对象得不同显示格式
                3、可将日志信息分割程多个文件记录
            2.2、流程：
                1、导入模块 importlogging
                2、选好需记录日志位置（日志可封装成函数）
                3、通过日志器logger实例化一个对象log_obj = logging.getLogger()
                4、设置日志器处理日志消息的最低级别（全局）可以不改，默认debug
                    log_obj.setLevel(logging.DEBUG)
                5、创建句柄/屏幕句柄/等其它需分割日志句柄
                    file_handler2 = loging.FileHandler('errer.log')
                6、设置日志显示格式化（可为每个handler设，也可共用）
                7、设置各个handler的日志格式化模式
                8、设置各个handler的日志级别，必须高于日志器
                9、对象即日志器与句柄即处理器县官取
                10、设置各日志级别message
    随机数模块：random模块
        random.random()  0~1 之间的随机小数
        random.uniform(x,y) x~y之间的整数小数，无限循环
        random.randint(x,y)  [x,y] x~y之间的整数
        random.randrange(x,y,z) [x,y) 步长为z，整数
        random.chioce(callable)  随机取出一个元素
        random.sample(list,sep)  取出指定sep个元素
        random.suffle(list)  随机打乱
    模块搜索路劲：
        python启动加载模块，sys
        第一次导入时，会检查是否已经导入，已导入不再加载，直接引用，没有先找内建，后path找sys.path
    sys模块：
        sys.platform  打印平台名称
        sys.version  python解释器名称
        sys.path     当前python程序初始化环境变量
        临时更改
        sys.path.append(path)
        sya.path.insert(0,path)  插入
    os与sys的区别，什么时候用
    时间模块time



python异常处理：
    错误分类：
        1、语法错误：你程序未执行之前，python已提示
        2、逻辑错误
    异常：
        由错误造成的信号，且出现终止程序
        valueError   IndexError ……
        由错误引发的，而且出现异常就会终止异常
        异常就会终止程序，用户体验差
        让代码不冗余
        try .... except
        try .... except ....else... 不发生异常则else
        try ....except....fanally


网络编程，并发编程：
    同步控制：锁、信号量、池、事件
    join  同步控制，获得结果
    锁     数据安全
    池     解决并发

python版本控制：virtualenv   pipenv

iO多路复用：
io多路复用是操作系统提供的一种监听网络Io操作的机制
监听三个列表，分别为读，写，条件事件对象
当某一个列表有的对应的事件发生的时候，操作胸痛通知(select通知)应用程序
操作胸痛根据返回的内容做具体操作




py2与py3区别：
89年创立，08年出2.7和3.0

1、打印，py2 print可以不用括号，也可以用括号，py3必须用括号
2、除法，py2 / 除法得 int， py3得float
3、编码，py2 默认ascii，py3 默认utf-8
4、range，py2 有range和xrange，py3只有range可迭代
5、输出，py2 为raw_input()返回为str，input如果输入是int，返回值类型也为int,py3为input（）返回得数据类型始终为str

--  node -v  查看Node.js 版本信息

　　--  npm -v  查看npm版本信息

更新npm到指定版本：

　　--  npm install npm@5.3.0 -g

　　-- npm install npm@latest -g 更新最新的稳定版本
```