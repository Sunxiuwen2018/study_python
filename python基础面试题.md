1. 为什么学习Python？

```
IT行业是目前乃至以后的趋势，并且我也对IT行业有浓厚的兴趣，现在都是实体与互联网相结合，生活中小到扫码付款，大到淘宝京东，甚至买房都可以在通过互联网实现，而我从知乎和其他网站了解到的，在众多语言当中，python是未来语言，python不仅可以写网站，前后端交互，还涉及人工智能,金融,爬虫,人脸识别等等，美国早在几年前就将python纳入大学的基本课程，现在中国杭州和一些试点城市，从小学都开始普及Python课程，所以我要学习Python。
```

1. 通过什么途径学习的Python？

```
在学校期间无意间看到别人在弄这个人脸识别,通过一张照片能分辨出性别,年龄范围和颜值,然后就从网上搜了一下python,发现有好多的文档和路飞学诚等都有python的课程与讲解，让后我通过阅读相关书籍以及网上的一些课程进行学习。
```

1. Python和Java、PHP、C、C#、C++等其他语言的对比？

```
python和以上语言对比,第一点开发效率快,有非常强大的第三方模块支持,第二点语法清晰简单,第三点有非常强大的跨平台和扩展性
```

1. 简述解释型和编译型编程语言？

```
编译型：运行前先由编译器将高级语言代码编译为对应机器的cpu汇编指令集，再由汇编器汇编为目标机器码，生成可执行文件，然最后运行生成的可执行文件。最典型的代表语言为C/C++，一般生成的可执行文件及.exe文件。 

解释型：在运行时由翻译器将高级语言代码翻译成易于执行的中间代码，并由解释器（例如浏览器、虚拟机）逐一将该中间代码解释成机器码并执行（可看做是将编译、运行合二为一了）。最典型的代表语言为JavaScript、Python、Ruby和Perl等。 

总结:
    编译型的语言就类似于去饭店点菜,菜上来了就吃
    解释型的语言就类似于去饭店吃火锅,以一边吃一边涮
```

1. Python解释器种类以及特点？

```
 CPython

  当 从Python官方网站下载并安装好Python2.7后，就直接获得了一个官方版本的解释器：Cpython，这个解释器是用C语言开发的，所以叫 CPython，在命名行下运行python，就是启动CPython解释器，CPython是使用最广的Python解释器。

  IPython

  IPython是基于CPython之上的一个交互式解释器，也就是说，IPython只是在交互方式上有所增强，但是执行Python代码的功能和CPython是完全一样的，好比很多国产浏览器虽然外观不同，但内核其实是调用了IE。

  PyPy

  PyPy是另一个Python解释器，它的目标是执行速度，PyPy采用JIT技术，对Python代码进行动态编译，所以可以显著提高Python代码的执行速度。

  Jython

  Jython是运行在Java平台上的Python解释器，可以直接把Python代码编译成Java字节码执行。

  IronPython

  IronPython和Jython类似，只不过IronPython是运行在微软.Net平台上的Python解释器，可以直接把Python代码编译成.Net的字节码。

  在Python的解释器中，使用广泛的是CPython，对于Python的编译，除了可以采用以上解释器进行编译外，技术高超的开发者还可以按照自己的需求自行编写Python解释器来执行Python代码，十分的方便！
  
Qpython
安卓端的一个python解释器,Qpython是一种通用叫法,其实它分为两款,分别是Qpython和Qpython3分别对应的是python2和python3
```

1. b、B、KB、MB、GB 的关系？

```
1 byte (B) = 8 bits (b) 字节=8个二进制位 
1 Kilobyte(K/KB)=2^10 bytes=1,024 bytes 千字节 
1 Megabyte(M/MB)=2^20 bytes=1,048,576 bytes 兆字节 
1 Gigabyte(G/GB)=2^30 bytes=1,073,741,824 bytes 千兆字节 
1 Terabyte(T/TB)=2^40 bytes=1,099,511,627,776 bytes吉字节
```

1. 请至少列举5个 PEP8 规范（越多越好）。

```
1.缩进。4个空格的缩进（编辑器都可以完成此功能），不使用Tap，更不能混合使用Tap和空格。

2.每行最大长度79，换行可以使用反斜杠，最好使用圆括号。换行点要在操作符的后边敲回车。

3.类和top-level函数定义之间空两行；类中的方法定义之间空一行；函数内逻辑无关段落之间空一行；其他地方尽量不要再空行

4.注释 总体原则，错误的注释不如没有注释。所以当一段代码发生变化时，第一件事就是要修改注释！注释必须使用英文，最好是完整的句子，首字母大写，句后要有结束符，结束符后跟两个空格，开始下一句。如果是短语，可以省略结束符。
块注释，在一段代码前增加的注释。在‘#’后加一空格。段落之间以只有‘#’的行间隔。
行注释，在一句代码后加注释。比如：(但是这种方式尽量少使用)
避免无谓的注释

5.文档描述为所有的共有模块、函数、类、方法写docstrings；非共有的没有必要，但是可以写注释（在def的下一行）。
如果docstring要换行

6.命名规范总体原则，新编代码必须按下面命名风格进行，现有库的编码尽量保持风格。
尽量单独使用小写字母‘l’，大写字母‘O’等容易混淆的字母。
模块命名尽量短小，使用全部小写的方式，可以使用下划线。
包命名尽量短小，使用全部小写的方式，不可以使用下划线。
类的命名使用CapWords的方式，模块内部使用的类采用_CapWords的方式。
异常命名使用CapWords+Error后缀的方式。
全局变量尽量只在模块内有效，类似C语言中的static。实现方法有两种，一是all机制;二是前缀一个下划线。
函数命名使用全部小写的方式，可以使用下划线。
常量命名使用全部大写的方式，可以使用下划线。
类的属性（方法和变量）命名使用全部小写的方式，可以使用下划线。
类的属性有3种作用域public、non-public和subclass API，可以理解成C++中的public、private、protected，non-public属性前，前缀一条下划线。
类的属性若与关键字名字冲突，后缀一下划线，尽量不要使用缩略等其他方式。
为避免与子类属性命名冲突，在类的一些属性前，前缀两条下划线。比如：类Foo中声明__a,访问时，只能通过Foo._Foo__a，避免歧义。如果子类也叫Foo，那就无能为力了。
类的方法第一个参数必须是self，而静态方法第一个参数必须是cls。

具体详情请查看  ---> https://www.python.org/dev/peps/pep-0008/
```

1. 通过代码实现如下转换：

```
二进制转换成十进制：v = "0b1111011"
十进制转换成二进制：v = 18  
八进制转换成十进制：v = "011"  
十进制转换成八进制：v = 30  
十六进制转换成十进制：v = "0x12"  
十进制转换成十六进制：v = 87
```

```
v = "0b1111011"
int(v,2)

v = "18"
bin(int(v))

v = "011"
int(v,8)

v = 30
oct(int(v))

v = "0x12"
int(v,16)

v = 87
hex(v)
```

### 9.请编写一个函数实现将IP地址转换成一个整数。

```
如 10.3.9.12 转换规则为：
        10            00001010
         3            00000011 
         9            00001001
        12            00001100 
再将以上二进制拼接起来计算十进制结果：00001010 00000011 00001001 00001100 = ？
```

```python
ip = '10.3.9.12'
ip_list = ip.split('.')
num = []
for i in ip_list:
    i = int(i)
    num.append(format(i,'08b'))  # 格式化为2进制
bin_str = ''.join(num)
ret = int(bin_str,2)
print(ret)
```

### 10.python递归的最大层数？

```
最多能打印到 998
然后就会抛出RuntimeError: maximum recursion depth exceeded” 的错误

官方:
but in 2.0 the maximum recursion depth can be read and modified using sys.getrecursionlimit() andsys.setrecursionlimit(). The default value is 1000
```

### 11.求结果

```
v1 = 1 or 3 
v2 = 1 and 3 
v3 = 0 and 2 and 1
v4 = 0 and 2 or 1
v5 = 0 and 2 or 1 or 4
v6 = 0 or False and 1
```



```
1
3
0
1
1
False

结论：
1，他是有优先级顺序的，() > not > and > or ，按照优先级的高低，先计算优先级高的，将所有同级的计算完毕之后，在计算下一个级别的。
2，遵循这个方式： x or y  if x is True return x else return y .  
                x and y if x is True,return y else return x.
                x,y是数字，对于数字来说，非零即True,零即False。
咱们用v5 = 0 and 2 or 1 or 4 举例：
  首先这是两个级别，先算and：0 and 2 结果为0，然后剩下两个or 则从左至右依次计算，即：0 or 1 为 1，然后 1 or 4 为 1 ，所以这个结果为1.
```

### 12.ascii、unicode、utf-8、gbk 区别？

```
ASCII：

       由于计算机是美国人发明的，因此最早只把127个字符编码到计算机里，即大小写英文字母、数字、部分西欧字符和一些常用符号等。
ASCII码只需要1个字节（1byte=8bit）即可存放。

Unicode：

       如果想要处理非ASCII码表里的字符，显然1个字节是不够用的，因此，中国将中文字符编入了GB2312，日本将日文编入了Shift-JIS、韩国将韩文编入了Euc-kr，其他国家也有自己的编码，这样做的结果就是如果将含有多种编码格式的字符存放到同一个文本里，就会出现令人头痛的乱码问题（乱码问题本质就是解码的字典不同导致的。）

       鉴于上述原因，Unicode应运而生，它将所有字符都统一编入在一个字典里，之前用2个字节表示一个字符，后来发现两个字节不能表示全部字符后来改为4个字节表示一个字符，这样再也不用担心不同的字符集里的字符放在一起出现乱码的问题了。所以现在Unicode是有两个版本，之前的版本是2个字节表示一个字符，现在是4个字节表示一个字符，python3x使用的unicode全部是4个字节表示一个字符。

       Unicode和ASCII的区别就是：
       1，前者是用4个字节（或者2个字节）表示一个字符，后者是用1个字节表示的。
       2，前者叫万国码，包含有记录的所有的文字，而后者只包含数字，字母，特殊符号。


UTF-8：

        Unicode的出现似乎完美的解决了乱码问题，但是会带来一个新的问题：如果你的文本基本全是英文或数字，那么用Unicode存储会比ASCII存储多出几倍的空间，而且传输起来也不划算（要占用更多的带宽），怎么办呢？能不能根据字符的种类来决定采取占用的字节呢？

          回答是可以的，这就是UTF-8，也就是“可变长编码”，它能根据Unicode字符的种类来决定存储的长度，例如：常用的英文编码成1个字节，汉字编码成3个字节
如果你的文本里含有大量的英文字符、数字、常用符号，那么使用UTF-8将会节省大量的存储空间，传输起来也会快很多

GB2312和GBK：

      GB2312是中国自己发布的一套汉字编码规范，于1980年发布。而GBK是中国在1995年颁布的，它向下兼容了GB2312，还向上兼容了ISO国际标准(ANSI)，包含的字符更多了。但是无论是GBK,还是GB2312,都只是'国标'，他只包含常用中文，数字，字母，特殊符号。
```

### 13.字节码和机器码的区别？

```
机器码

机器码 学名机器语言指令，白话文就是计算机能够识别的一种指令.比如
我们在程序中写hello world其实就是将我们人类能够识别的内容转换成计算机能够识别的01010101

字节码 组成的二进制文件。字节码是一种中间码，它比机器码更抽象，需要直译器转译后才能成为机器码的中间代码。

总结：
    机器码就是交于cpu运行的一种文件
    字节码是一种中间状态（中间码）的二进制文件,需要转译后才能成为机器码。

```

### 14.三元运算规则以及应用场景？

```
  简化if语句
  python语言:
  规则 表达式 if 真 else 假
  if else这种运算符会将某个条件作两种处理，如果满足条件的话就执行第一个结果，如果不满足的话就执行另外一个结果，例如：
  
  name = input('>>>')
  msg = '追日' if name == '夸父' else '跑丢了'
  print(msg)

  这条语句的意思是，让用户输入内容,如果内容是夸父就把夸父赋值到msg这个变量中,否则就就把跑丢了赋值到msg中,最后打印msg这个变量查看；

  JavaScript
  规则 表达式 ？ 真 ：假
    ?:符号表示的，具体的含义其实就和if-else结构的含义差不多，这种运算符会将某个条件作两种处理，如果满足条件的话就执行第一个结果，如果不满足的话就执行另外一个结果，例如： 
  
  Int A,B,C; 
  A=2; 
  B=3; 
  C=A>B ? 100 :200; 
  这条语句的意思是，如果A>B的话，就将100赋给C，否则就将200赋给C；
 
```

### 15.列举 Python2和Python3的区别？

```
py2和py3:
  1. 文件操作：  xreadlines

  f = open('x.log','rb')

  for line in f.xreadlines():
  print(line)

  f.close()

  2. 字符串：
  py2:
  str: 字符串   -> 字节
  unicode: u"sdfsdf" 
  py3:
    bytes:
  str:
  3. 默认解释器编码
  py2: ascii
  py3: unicode

  5. 
  py2: range/xrange 
  py3:       range 

  6. 
  py2: int / long
  py3: int 

  7. input/raw_input 

  8. 
  py2: yield
  py3: yield/yield from 

  9. 
  py2: 新式类继承object和经典类不用继承
  py3: 新式类默认继承object
```

1. 用一行代码实现数值交换：

```
a = 1
b = 2
a,b = b,a
```

1. Python3和Python2中 int 和 long的区别？

```
python3 彻底废弃了 long+int 双整数实现的方法, 统一为 int , 支持高精度整数运算.
```

1. xrange和range的区别？

```
python2中xrange和python3中range 的用法完全相同，但是返回的是一个生成器。 
```

1. 文件操作时：xreadlines和readlines的区别？

```
   1) read([size])方法从文件当前位置起读取size个字节，若无参数size，则表示读取至文件结束为止，它范围为字符串对象
    2) 从字面意思可以看出，该方法每次读出一行内容，所以，读取时占用内存小，比较适合大文件，该方法返回一个字符串对象。
    3) readlines()方法读取整个文件所有行，保存在一个列表(list)变量中，每行作为一个元素，但读取大文件会比较占内存。
    4）xreadlines()方法则是直接返回一个iter迭代器，在python2.3之后就不推荐这种方法了。
    for line in f:
      拿到每一行数据
```

1. 列举布尔值为False的常见值？

```
  布尔型，False表示False，其他为True
  整数和浮点数，0表示False，其他为True
  字符串和类字符串类型（包括bytes和unicode），空字符串表示False，其他为True
  序列类型（包括tuple，list，dict，set等），空表示False，非空表示True
  None永远表示False
```

1. 字符串、列表、元组、字典每个常用的5个方法？

```
  - 字符串  split/strip/replace/find/index ...
  - 列表     append/extend/insert/push/pop/reverse/sort ...
  - 元组     len/max/min/count/index ...
  - 字典     keys/values/pop/clear/del ...
  - 集合  add/remove/clear/交集&、并集 |、差集 - 
  
  扩展: 
  - collections  Python内建的一个集合模块，提供了许多有用的集合类。
      1.Counter是一个简单的计数器，例如，统计字符出现的个数;
      2.OrderedDict可以实现一个FIFO（先进先出）的dict，当容量超出限制时，先删除最早添加的Key;
      3.deque是为了高效实现插入和删除操作的双向列表;
      4.defaultdict使用dict时，如果引用的Key不存在，就会抛出KeyError。如果希望key不存在时，返回一个默认值，就可以用defaultdict;
```

1. lambda表达式格式以及应用场景？

```
 省去函数命名的烦恼
 lambda存在意义就是对简单函数的简洁表示
 列表生成式配合
  min/max/filter/map/sorted/reduce  
  
  min:(最小的)
      li = [-1,2,-3,4]
      s = min(li,key=lambda x:x)
  max:(最大的)
      li = [-1,2,-3,4]
      s = max(li,key=lambda x:x)
      print(s)
  filter:(过滤)
      li = [-1,2,-3,4,8,9,-4]
      s = list(filter(lambda x:x >3,li))
  map:(映射)
      li = [1,2,3]
      s = list(map(lambda x,y,z:x*y*z,li,li,li))
  sorted:(排序)
    dic = {'a1':44,'a2':33}
    s = sorted(dic.items(),key=lambda x:x[1])
    这样是将按照字典的值中小的排序,返回的是一个列表中有多个元祖
    s = sorted(dic.items(),key=lambda x:x[1],reverse=True)   
    这样是将按照字典的值中大的排序,返回的是一个列表中有多个元祖  
    
  reduce:(归纳)  
    python2:
        python2中reduce是内置方法
        li = [6,2,3,4,5]
        s = reduce(lambda x,y:x+y,li)
        
    python3:
        python3中reduce方法内置到functools中
        from functools import reduce
        li = [6,2,3,4,5]
        s = reduce(lambda x,y:x+y,li)

  
```

1. pass的作用？

```
当你在编写一个程序时，执行语句部分思路还没有完成，这时你可以用pass语句来占位，也可以当做是一个标记，是要过后来完成的代码。

程序当中 ... 功能和pass功能一样
```

1. *arg和**kwarg作用

```
  *args：（表示的就是将实参中按照位置传值，多出来的值都给args，且以元组的方式呈现）在形参表示聚合, 在实参表示打散
  **kwargs：（表示的就是实参中按照关键字传值把多余的传值以字典的方式呈现）在形参表示聚合, 在实参表示打散

```

1. is和==的区别

```
 is 比较的是两个实例对象是不是完全相同，它们是不是同一个对象，占用的内存地址是否相同。莱布尼茨说过：“世界上没有两片完全相同的叶子”，这个is正是这样的比较，比较是不是同一片叶子（即比较的id是否相同，这id类似于人的身份证标识）。

  == 比较的是两个对象的内容是否相等，即内存地址可以不一样，内容一样就可以了。这里比较的并非是同一片叶子，可能叶子的种类或者脉络相同就可以了。默认会调用对象的 __eq__()方法。
  
 总结:
     == 是比较这俩个人长的是不是一样
     is 是比较这俩个人是不是一个人
```

1. 简述Python的深浅拷贝以及应用场景？

```
  Python采用基于值得内存管理模式，赋值语句的执行过程是：首先把等号右侧标识的表达式计算出来，然后在内存中找一个位置把值存放进去，最后创建变量并指向这个内存地址。Python中的变量并不直接存储值，而是存储了值的内存地址或者引用
  简单地说，浅拷贝只拷贝一层（如果有嵌套），深拷贝拷贝所有层。
  一层的情况：
    import copy

    # 浅拷贝  

    li1 = [1, 2, 3]
    li2 = li1.copy()
    li1.append(4)
    print(li1, li2)  # [1, 2, 3, 4] [1, 2, 3]

    # 深拷贝

    li1 = [1, 2, 3]
    li2 = copy.deepcopy(li1)
    li1.append(4)
    print(li1, li2)  # [1, 2, 3, 4] [1, 2, 3]
  多层的情况：
    import copy

    # 浅拷贝

    li1 = [1, 2, 3, [4, 5], 6]
    li2 = li1.copy()
    li1[3].append(7)
    print(li1, li2)  # [1, 2, 3, [4, 5, 7], 6] [1, 2, 3, [4, 5, 7], 6]

    # 深拷贝

    li1 = [1, 2, 3, [4, 5], 6]
    li2 = copy.deepcopy(li1)
    li1[3].append(7)
    print(li1, li2)  # [1, 2, 3, [4, 5, 7], 6] [1, 2, 3, [4, 5], 6]
    
    应用场景：项目中的配置文件。
```

1. Python垃圾回收机制？

```
Python GC主要使用引用计数（reference counting）来跟踪和回收垃圾。在引用计数的基础上，通过“标记-清除”（mark and sweep）解决容器对象可能产生的循环引用问题，通过“分代回收”（generation collection）以空间换时间的方法提高垃圾回收效率。

  1 引用计数

  PyObject是每个对象必有的内容，其中ob_refcnt就是做为引用计数。当一个对象有新的引用时，它的ob_refcnt就会增加，当引用它的对象被删除，它的ob_refcnt就会减少.引用计数为0时，该对象生命就结束了。

  优点:

  简单 实时性 缺点:

  维护引用计数消耗资源 循环引用

  2 标记-清除机制

  基本思路是先按需分配，等到没有空闲内存的时候从寄存器和程序栈上的引用出发，遍历以对象为节点、以引用为边构成的图，把所有可以访问到的对象打上标记，然后清扫一遍内存空间，把所有没标记的对象释放。

  3 分代技术

  分代回收的整体思想是：将系统中的所有内存块根据其存活时间划分为不同的集合，每个集合就成为一个“代”，垃圾收集频率随着“代”的存活时间的增大而减小，存活时间通常利用经过几次垃圾回收来度量。

  Python默认定义了三代对象集合，索引数越大，对象存活时间越长。

  http://python.jobbole.com/82061/
```

1. Python的可变类型和不可变类型？

```
  在Python中不可变对象指：一旦创建就不可修改的对象，包括字符串，元组
  ，数字，布尔值

  在Python中可变对象是指：可以修改的对象，包括：列表、字典、集合
```

1. 求可变数据类型结果

```
   v = dict.fromkeys(['k1','k2'],[])  
   v['k1'].append(666)
   print(v) 
   v['k1'] = 777
   print(v)
    
  {'k1': [666], 'k2': [666]}
  {'k1': 777, 'k2': [666]}
   因为fromkeys设置的值是一个列表,字典中的每个健对应的值都是共用的一个列表所以才会出现上边的现象.下边的是重新对k1这个健重新复制
```

1. 求匿名函数结果

```
def num():
    return [lambda x: x*i for i in range(4)]
print([m(2) for m in num()])
```

```
[6, 6, 6, 6]
# 匿名函数某面试题题详解
def mu():  # 上边函数拆解后是这种结构
    l = []  # 定义一个列表
    for i in range(4):  # for循环4次
        def fun(x):  # 代码不执行
            return i * x  # 代码不执行

        l.append(fun)  # 列表中添加进去了4个未执行的函数，当列表中的函数被调用时，才会去内存中找i，此时的i是for循环的最后一位元素。
    return l  # 返回此列表


```

2. 生成器扩展面试题

   ```pyton
   def add(n,i):
       return n+i
   
   def test():
       for i in range(4):
           yield i
   
   g=test()
   for n in [1,10]:
       g=(add(n,i) for i in g)
   
   print(list(g))  ==》[20,21,22,23]
   ```

   ![1545827928523](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1545827928523.png)

1. 列举常见的内置函数？

```

    float(x)  # 把x转换成浮点数
    str(x)   # 转换成字符串
    list(x)  # 转换成列表
    tuple(x) # 转换成元组
   
     
    进制相互转换
     r= bin(10) #二进制
     r= int(10) #十进制

     r = oct(10) #八进制
     r = hex(10) #十六进制
     i= int("11",base=10)#进制间的相互转换base后跟 2/8/10/16
     
    chr(x)//返回x对应的字符，如chr(65)返回‘A'
    ord(x)//返回字符对应的ASC码数字编号，如ord('A')返回65
    abs() #绝对值
    input() # 程序交互
    id() # 查看内存地址
    enumerate() #枚举
    eval() #执行一个字符串表达式
    max() # 求最大
    min() # 求最小
    sum() # 求和
    range() # 范围
    type() # 查看数据类型
    len() #获取数据类型的长度
    zip（）
    sorted（）
    reversed（）
    filter（）
    
```

1. filter、map、reduce的作用？

```
  filter:对于序列中的元素进行筛选，最终获取符合条件的序列
  map:遍历序列，对序列中每个元素进行操作，最终获取新的序列
  reduce:对于序列内所有元素进行累计操作
```

1. 一行代码实现9*9乘法表

```
print("\n".join("\t".join(["%s*%s=%s" %(x,y,x*y) for y in range(1, x+1)]) for x in range(1, 10)) )
```

1. 如何安装第三方模块？以及用过哪些第三方模块？

```
  - pip包管理器
      pip install 模块名
  - 源码安装
      - 下载->解压->cd 到对应路径
      - python setup.py build
      - python setup.py install 
  
  requests
  selenium
  urllib3
  pymysql
  redis
  celery
  beautifulsoup4
  sqlarchmy
  xlrd
  gevent
 
```

1. 常用模块有那些？

```
- re/time/random/json/logging/os/sys/requests/beautifulsoup4/requests
```

1. re的match和search的区别？

```
re.match只匹配字符串的开始，如果字符串开始不符合正则表达式，则匹配失败，函数返回None；
re.search匹配整个字符串，直到找到一个匹配。
```

1. 什么是正则的贪婪匹配？

```
正则表达式通常用于在文本中查找匹配的字符串。Python里数量词默认是贪婪的（在少数语言里也可能是默认非贪婪），总是尝试匹配尽可能多的字符；非贪婪则相反，总是尝试匹配尽可能少的字符。在"*","+","{m,n}"后面加上？，使贪婪变成非贪婪。
```

1. 求结果： a. [ i % 2 for i in range(10) ] b. ( i % 2 for i in range(10) )

```
  [ i % 2 for i in range(10) ]  
  # [0, 1, 0, 1, 0, 1, 0, 1, 0, 1]
  
  ( i % 2 for i in range(10) )  
  # <generator object <genexpr> at 0x0000000003180FC0>
```

1. 求结果： a. 1 or 2 b. 1 and 2 c. 1 < (2==2) d. 1 < 2 == 2

```
  1
  2
  False
  True
```

1. def func(a,b=[]) 这种写法有什么坑？

```
  def func(a, b=[]):
      b.append(a)
      return b
   
   
  s = func(1)
  print(s)  # [1]
  s = func(1)
  print(s)  # [1, 1]
   
  # 第二次调用的时候 b的初始值是[1]了
  
  默认值参数在使用的时候每次都是使用的同一个对象. 所以当默认值参数是可变的数据类型的时候需要我们注意. 如果对默认值参数进行了改变. 那么其他函数使用的时候是被改变的结果.默认值参数使用的是同一个对象 
```

1. 如何实现"1,2,3"变成['1','2','3'] ?

```
  "1,2,3".split(",")
```

1. 如何实现['1','2','3']变成[1,2,3]?

```
 [int(x) for x in ['1','2','3']]
 map(lambda x: int(x), ['1','2','3'])
```

1. 比较： a = [1,2,3] 和 b = [(1),(2),(3) ] 以及 b = [(1,),(2,),(3,) ] 的区别？

```
  前两个列表内是int
  最后一个列表内是元组
  
  (数据) ==> 数据
  (数据,) ==> 元组, 元组内`12344`只有一个元素
```

1. 如何用一行代码生成[1,4,9,16,25,36,49,64,81,100] ?

```
  [i*i for i in range(11)]
```

1. 一行代码实现删除列表中重复的值 ?

```
list(set([1, 2, 3, 4, 45, 1, 2, 343, 2, 2]))
```

1. 如何在函数中设置一个全局变量 ?

```
def func():
    global a
    
func()

global可以在局部使用全局中的变量, 如果全局中没有这个变量, 那么可以将一个局部变量升华成全局变量, 总之,使用global 那这个变量一定是全局的.
```

1. logging模块的作用？以及应用场景？

```
logging模块是Python内置的标准模块，主要用于输出运行日志，可以设置输出日志的等级、日志保存路径、日志文件回滚等；相比print，具备如下优点：

    可以通过设置不同的日志等级，在release版本中只输出重要信息，而不必显示大量的调试信息；

    print将所有信息都输出到标准输出中，严重影响开发者从标准输出中查看其它数据；logging则可以由开发者决定将信息输出到什么地方，以及怎么输出。

```

1. 编写一个栈

```
# 先进后出 砌墙的砖头
  class Stack():
    def __init__(self, size):
        self.size = size
        self.stack = []
        self.top = 0 # 栈顶指针

    # 入栈之前检查栈是否已满
    def push(self, x):
        if self.isfull():
            raise Exception("stack is full")
        else:
            self.stack.insert(self.top, x)
            self.top = self.top + 1

    # 出栈之前检查栈是否为空
    def pop(self):
        if self.isempty():
            raise Exception("stack is empty")
        else:
            self.top = self.top - 1
            return self.stack.pop()

    def isfull(self):
        return self.top == self.size

    def isempty(self):
        return self.top == 0

    def showStack(self):
        return self.stack


```

1. 字符串格式化有哪些方式?

```
Python的字符串格式化有三种方式:%s f'{变量}' format()
 
name = "葫芦娃"
age = 28
hobby = "吃西瓜"
s1 = "我叫%s, 我今年%d岁了, 我喜欢%s" % (name, age, hobby)
s2 = "我叫{name}, 我今年{age}岁了, 我喜欢{hobby}".format(name=name, age=age, hobby=hobby)

s3 = f"我叫{name}, 我今年{age}岁了, 我喜欢{hobby}"

```

1. 简述 生成器、迭代器、可迭代对象 以及应用场景？

```
生成器, 本质是迭代器.当我们需要用到大量的数据, 并且分批量处理的时候可以考虑使用生成器, 生成器一般很少占用内存. 

迭代器, 迭代器遵循可迭代协议, 当需要对某数据类型进行遍历的时候可以给出该对象的迭代器. 就可以统一使用迭代器的规则来进行遍历数据.

可迭代对象, 可迭代对象表示可以使用迭代器的方式来完成数据的遍历

一般而言, 可迭代对象都会配备相对应的迭代器. 
list -> list_iterator
set -> set_iterator
tuple -> tuple_iterator

如果是用户自己定义的可迭代该象, 那一般用户也可以自己写出自己定义的迭代器
from collections import Iterable
from collections import Iterator

class MyIterator(Iterator):
    def __init__(self, arr):
        self.arr = arr
        self.index = 0
    def __next__(self):
        if self.index > len(self.arr) - 1:
            raise StopIteration
        else:
            self.index += 1
            return self.arr[self.index - 1]

class MyIterable(Iterable):
    def __init__(self, arr):
        self.arr = arr
    def __iter__(self):
        return MyIterator(self.arr)



for i in MyIterable([1, 2, 3, 4, 5]):
    print(i)

应用场景：爬虫用过yield，路飞项目redis构建了一个生成器，pickle取对象用过生成器。
```

1. 实现二分法查找

```
def binary_search(lst, n, left, right):
    if left <= right:
        mid = (left+right) // 2
        if n < lst[mid]:
            right = mid - 1
        elif n > lst[mid]:
            left = mid + 1
        else:
            return mid
        return binary_search(lst, n, left, right)    
    else:
        return -1
```

1. 谈谈你对闭包的理解？

```
闭包就是内层函数对外层函数中的局部变量的引用，并且返回内部的函数名。
闭包作用: 
   1. 可以保护变量不被侵占修改
   2. 可以让一个变量常驻内存
   
   # 此时a是在函数内部的. 不会被外界所干扰, 
   # 为了下面两个函数正常运行, a必须常驻内存
   def fun():
     a = 100
     def func_inner_1():
         print(a)
     def func_inner_2():
         print(a)
       
```

1. 面向对象的三个特征

```
封装: 将一个对象的数据集合在一个对象中. 方便使用和调取
继承: 在已知的类的基础上进一步对类进行扩展. 减少冗余代码的开发
多态: 同一个对象多种形态. 面向对象设计的灵魂所在. 将面向对象的思维进升华. 我们可以这样认为, 我们写的, 创建的, 使用的任何内容都是对象, 那我们就可以站在对象的角度来观察你写的内容. 例如, 猫是一种动物. 我们可以站在动物的角度来看猫, 这样猫就有了多种形态. 我们可以站在猫的角度来看猫, 也可以站在动物的角度来看这只猫. 但猫终归是猫. 本质还是原来那个对象. 

```

1. os和sys模块的作用？

```
    os就是一个普通的python库，用来向Python程序提供运行环境，特别是在文件系统、创建新进程、获取操作系统本身的一些信息（比如uname)，并屏蔽各种不同操作系统之间的细节差异。
    sys模块则是python程序用来请求解释器行为的接口。比如关于调试类的（trace, frames，except）等，profiling类（stats， getsizeof)，运行时环境类（python path, stderr, stdout)，解释器本身（如version）。inspect某种程度上可以看成是在sys提供的功能上的一个包装。
```

1. 如何生成一个随机数？

```
from random import randint
randint(10)
```

1. 如何使用python删除一个文件？

```
删除子目录
  os.rmdir( path )   # path: "要删除的子目录"

  产生异常的可能原因:
  (1) path 不存在
  (2) path 子目录中有文件或下级子目录
  (3) 没有操作权限或只读

  删除文件
  os.remove(   filename )   # filename: "要删除的文件名"

  产生异常的可能原因:
  (1) filename 不存在
  (2) 对filename文件， 没有操作权限或只读。
谈谈你对面向对象的理解? 面向对象. 一切皆为对象. 我们可以把生活中存在或者不存在的事物抽象成代码. 在代码的世界建立起一个对象的世界. 
和面向过程的对比: 面向过程,一切以我为中心,我先做xx, 然后做xxx, 最后做xxx. 这样的代码的可维护性是很差的. 只有你知道整个程序的流程. 面对象, 一切以对象为中心, 让对象去做相应的工作和事情, 我就解放出来了. 这样的模式可维护性会很高. 配合设计空间. 代码重用性更高.
    
```

1. Python面向对象中的继承有什么特点？

```
python支持多继承. 方法的查找路径根据C3算法来的. 
自动的拥有父类中的方法和属性. 
```

1. 面向对象深度优先和广度优先是什么？

```
python分为经典类和新式类
经典类的MRO根据数的深度优先去遍历
新式类使用的是C3算法来遍历的. 
```

1. 面向对象中super的作用？

```
我们都知道，在子类中如果有与父类同名的成员，那就会覆盖掉父类里的成员。那如果你想强制调用父类的成员呢？使用super()函数！这是一个非常重要的函数，最常见的就是通过super调用父类的实例化方法__init__！

  语法：super(子类名, self).方法名()，需要传入的是子类名和self，调用的是父类里的方法，按父类的方法需要传入参数。
  class A:
      def __init__(self, name):
          self.name = name
          print("父类的__init__方法被执行了！")
      def show(self):
          print("父类的show方法被执行了！")

  class B(A):
      def __init__(self, name, age):
          super(B, self).__init__(name=name)
          self.age = age

      def show(self):
          super(B, self).show()

  obj = B("jack", 18)
  obj.show()
  
 总结:  super 在子类中访问父类中的内容
 
super是查找MRO中的下一个
A->B->C->D->E
super(C, self).方法() 找到C的下一个. 执行该类中的方法
super().方法() 当前类的下一个. 执行该方法

```

1. 是否使用过functools中的函数？其作用是什么？

```
1.functools.partial
偏函数. 可以将函数的参数进行固定. 方便使用和调用
2.functools.wraps
可以把一个函数的基本信息进行重新定义. 在装饰器比较常用. 把装饰器中的inner函数改成被装饰的函数.
reduce 

```

1. 列举面向对象中带双下划线的特殊方法，如：__new__

```
__init__ :      构造函数，在生成对象时调用
  __del__ :       析构函数，释放对象时使用
  __repr__ :      打印，转换
  __setitem__ :   按照索引赋值
  __getitem__:    按照索引获取值
  __len__:        获得长度
  __cmp__:        比较运算
  __call__:       调用
  __add__:        加运算
  __sub__:        减运算
  __mul__:        乘运算
  __div__:        除运算
  __mod__:        求余运算
  __pow__:        幂
  
```

1. 如何判断是函数还是方法？

```
print(isinstance(obj.func, FunctionType))   # False
print(isinstance(obj.func, MethodType))    # True

  示例:
  class Foo(object):
      def __init__(self):
          self.name = 'lcg'
   
      def func(self):
          print(self.name)
   
   
  obj = Foo()
  print(obj.func)  # <bound method Foo.func of <__main__.Foo object at 0x000001ABC0F15F98>>
   
  print(Foo.func)  # <function Foo.func at 0x000001ABC1F45BF8>
   
  # ------------------------FunctionType, MethodType------------#
   
   
  from types import FunctionType, MethodType
   
  obj = Foo()
  print(isinstance(obj.func, FunctionType))  # False
  print(isinstance(obj.func, MethodType))  # True
   
  print(isinstance(Foo.func, FunctionType))  # True
  print(isinstance(Foo.func, MethodType))  # False
   
  # ------------------------------------------------------------#
  obj = Foo()
  Foo.func(obj)  # lcg
   
  obj = Foo()
  obj.func()  # lcg
   
  """
  注意：
      实例方法
        1. 类名.方法() 此时方法就是函数
        2. 对象.方法() 此时就是方法
      类方法
        任何情况都是方法
      静态方法
        任何情况都是函数
        
  """
```

1. 静态方法和类方法区别？

```
classmethod 必须有一个指向类对象的引用作为第一个参数，而 staticmethod 可以没有任何参数，静态方法是非绑定方法，类方法是绑定方法
  class Num:
      # 普通方法：能用Num调用而不能用实例化对象调用   
      def one():  
          print ('1')
   
      # 实例方法：能用实例化对象调用而不能用Num调用
      def two(self):
          print ('2')
   
      # 静态方法：能用Num和实例化对象调用
      @staticmethod 
      def three():  
          print ('3')
   
      # 类方法：第一个参数cls长什么样不重要，都是指Num类本身，调用时将Num类作为对象隐式地传入方法   
      @classmethod 
      def go(cls): 
          cls.three() 
   
  Num.one()          #1
  #Num.two()         #TypeError: two() missing 1 required positional argument: 'self'
  Num.three()        #3
  Num.go()           #3
   
  i=Num()                
  #i.one()           #TypeError: one() takes 0 positional arguments but 1 was given         
  i.two()            #2      
  i.three()          #3
  i.go()             #3 
```

1. 列举面向对象中的特殊成员以及应用场景

```
http://www.cnblogs.com/bainianminguo/p/8076329.html
```

1. 1,2,3,4,5 能组成多少个互不相同且无重复的三位数. 

```
方案一: 
  for x in range(1, 6):
      for y in range(1, 6):
          for z in range(1, 6):
              if (x != y) and (y != z) and (z != x):
                  i += 1
                  if i % 4:
                      print("%d%d%d" % (x, y, z), end=" | ")
                  else:
                      print("%d%d%d" % (x, y, z))
  print(i)
  
方案二:  
lst =  [1,2,3,4,5]
a = [(a, b, c) for a in lst for b in lst for c in lst if a!=b and b!=c and c!=a]
print(len(a))
print(a)

```

1. 什么是反射？以及应用场景？

```
 反射就是通过字符串的形式，导入模块；通过字符串的形式，去模块寻找指定函数，并执行。利用字符串的形式去对象（模块）中操作（查找/获取/删除/添加）成员，一种基于字符串的事件驱动！
  https://www.cnblogs.com/vipchenwei/p/6991209.html
```

1. metaclass作用？以及应用场景？

```
  metaclass用来指定类是由谁创建的。

  类的metaclass 默认是type。我们也可以指定类的metaclass值。
  http://www.cnblogs.com/0bug/p/8578747.html
```

1. 用尽量多的方法实现单例模式.

```
使用模块
使用 __new__
使用装饰器（decorator）
使用元类（metaclass）
```

1. 装饰器的写法以及应用场景。

```
装饰器: 
def wrapper(fn):
    def proxy(*args, **kwargs):
        '''before target'''
        ret = fn(*args, **kwargs)
        '''after target'''
        return ret
    return proxy

@wrapper
def func():
    pass

当需要给函数动态添加或删减功能的时候可以考虑使用装饰器. 装饰器符合面向对象编程思想的核心理念. 提高程序的可读性和可维护性, 并且在更新功能的时候更加容易. 
  
```

1. 异常处理写法以及如何主动抛出异常（应用场景）

```
python有两种处理异常的方案: 1. 异常处理 2.断言
try:
    1 / 3
except Exception as e:
    '''异常的父类，可以捕获所有的异常'''
else:
    '''保护不抛出异常的代码, 当try中无异常的时候执行'''
finally:
    '''最后总是要执行我'''


抛出异常: raise RuntimeError("who the hell are you?")

使用场景:
  如果你不想在异常发生时结束你的程序，只需在try里捕获它。

```

1. 什么是面向对象的mro

```
MRO(Method Resolution Order)主要用于在多继承时判断调的属性的路径. 在python中支持多继承. 当我们访问方法的时候根据MRO来判断具体执行的是哪个方法. 
用来计算继承顺序. 在早期的版本中MRO采用深度遍历方案. 在3.x版本中时候的是C3算法. 
```

1. isinstance作用以及应用场景？

```
isinstance是Python中的一个内建函数。是用来判断一个对象的类型.
```

1. 写代码LeetCode并实现:

```
Given an array of integers, return indices of the two numbers such that they add up to a specific target.You may assume that each input would 
have exactly one solution, and you may not use the same element twice.
Example: 
          Given nums = [2, 7, 11, 15], target = 9,
           Because nums[0] + nums[1] = 2 + 7 = 9, 
           return [0, 1]

Answer:
def func(lst ,target):
    gen = ((a, b, index_f, index_n) for index_f, a in enumerate(lst) 
    
    for a, b,index_f, index_n in gen:
        if a + b == target:
            return index_f, index_n
    else:
        print("没有")


lst = [3, 7, 9, 12, 18, 23] # 27
print(func(lst, target = int(input("请输入你的目标"))))
```

1. json序列化时，可以处理的数据类型有哪些？如何定制支持datetime类型？

```
自定义时间序列化转换器
import json
from json import JSONEncoder
from datetime import datetime
class ComplexEncoder(JSONEncoder):
    def default(self, obj):
        if isinstance(obj, datetime):
            return obj.strftime('%Y-%m-%d %H:%M:%S')
        else:
            return super(ComplexEncoder,self).default(obj)
d = { 'name':'alex','data':datetime.now()}
print(json.dumps(d,cls=ComplexEncoder))
# {"name": "alex", "data": "2018-05-18 19:52:05"}

```



1. json序列化时，默认遇到中文会转换成unicode，如果想要保留中文怎么办？

```
import json
a=json.dumps({"ddf":"你好"},ensure_ascii=False)
print(a) #{"ddf": "你好"}

在序列化时，中文汉字总是被转换为unicode码，在dumps函数中添加参数ensure_ascii=False即可解决。
```



1. 什么是断言？应用场景？

```
assert断言语句用来声明某个条件是真的，其作用是测试一个条件(condition)是否成立，如果不成立，则抛出异常。

断言跟异常的区别：
断言是用来检查非法情况而不是错误情况的，用来帮开发者快速定位问题的位置。
异常处理用于对程序发生异常情况的处理，增强程序的健壮性和容错性。
对一个函数而言，一般情况下，断言用于检查函数输入的合法性，要求输入满足一定的条件才能继续执行;
在函数执行过程中出现的异常情况使用异常来捕获。

```





1. 有用过with 语句吗？它的好处是什么？

```
with open() as f:
    # 文件相关操作
with的好处是当我们处理文件的时候不需要管理文件的关闭. 由with自动处理, 简化代码

```



1. 使用代码实现查看列举目录下的所有文件。

```
import os

def read(filepath, n):
    files = os.listdir(filepath)    # 获取到当前文件夹中的所有文件
    for f in files:    # 遍历文件夹中的文件, 这里获取的只是本层文件名
        fi_d = os.path.join(filepath,f)    # 加入文件夹 获取到文件夹+文件
        if os.path.isdir(fi_d): # 如果该路径下的文件是文件夹
            print("\t"*n, f)
            read(fi_d, n+1)     # 继续进行相同的操作
        else:
            print("\t"*n, f)   # 递归出口. 最终在这里隐含着return


#递归遍历目录下所有文件
read('../oldboy/', 0)

```



1. 简述 yield和yield from关键字。

```
yield 表示一个函数是生成器. 可以分段执行一个函数
yield from表示可以把一个可迭代对象转换成生成器

yield from iterable本质上等于for item in iterable: yield item的缩写版

使用示例:
  def func():
      yield from lst
  g = func()
  print(g.__next__())
  print(g.__next__())
  
面试真题：
[1，2，[3，[4，5]]，6，[7，]]  用生成器将其生成[1，2，3，4，5，6，7] 

 def func3(x):
    for i in x:
        if isinstance(i, collections.Iterable):
            yield from func3(i)
        else:
            yield i


a = [1, 2, [3, [4, 5]], 6, [7, ]]
ret3 = list(func3(a))
print(ret3)

   
```