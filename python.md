# <center>Python笔记</ceneter>

## Python简介
### Python历史
Python 是由 Guido van Rossum 在八十年代末和九十年代初，在荷兰国家数学和计算机科学研究所设计出来的。
Python 本身也是由诸多其他语言发展而来的,这包括 ABC、Modula-3、C、C++、Algol-68、SmallTalk、Unix shell 和其他的脚本语言等等。
像 Perl 语言一样，Python 源代码同样遵循 GPL(GNU General Public License)协议。
现在 Python 是由一个核心开发团队在维护，Guido van Rossum 仍然占据着至关重要的作用，指导其进展。

目前流行的是Python2.x，最新的Python目前是Python3.x。
### Python特征
1. 易于学习：Python有相对较少的关键字，结构简单，和一个明确定义的语法，学习起来更加简单。
2. 易于阅读：Python代码定义的更清晰。
3. 易于维护：Python的成功在于它的源代码是相当容易维护的。
4. 一个广泛的标准库：Python的最大的优势之一是丰富的库，跨平台的，在UNIX，Windows和Macintosh兼容很好。
5. 互动模式：互动模式的支持，您可以从终端输入执行代码并获得结果的语言，互动的测试和调试代码片断。
6. 可移植：基于其开放源代码的特性，Python已经被移植（也就是使其工作）到许多平台。
7. 可扩展：如果你需要一段运行很快的关键代码，或者是想要编写一些不愿开放的算法，你可以使用C或C++完成那部分程序，然后从你的Python程序中调用。
8. 数据库：Python提供所有主要的商业数据库的接口。
9. GUI编程：Python支持GUI可以创建和移植到许多系统调用。
10. 可嵌入: 你可以将Python嵌入到C/C++程序，让你的程序的用户获得"脚本化"的能力。
11. 解释性和编译性：Python语言写的程序不需要编译成二进制代码，可以直接运从源代码运行程序，但是需要解释器。这点类似于Java，或者Matlab。Python也可以编译后执行程序，这样速度优于直接从源代码执行的速度。
12. 面向对象编程：Python支持面向过程的编程也支持面向对象的编程。与其他的语言如C++和Java相比，Python以一种非常强大而又简单的方式实现面向对象编程。
13. 高级语言：使用Python语言编写程序，无需考虑诸如管理内存一类的底层。
14. 丰富的库：

### Python应用场景
国外：
- Google：实现Web爬虫和搜索引擎中的很多组件
- YaHoo： 管理讨论组以及其他技术
- NASA：NASA在他的几个系统中既实用Python开发，又作为脚本语言
- YouTube： 视频分享服务大部分都是由Python编写的

国内：
- 豆瓣：前后台使用Python
- 还有其他很多的现在也是用Python作为前后台开发的

## Python安装
### Linux下Python环境搭建
大多数Linux发行版都默认自带Python，一般都是Python2.x
如果没有安装可以通过源码进行安装：
   ```python
    # ./configure --prefix=/usr/local
    # make && make install
    # make clean 
    # make distclean
   ```
然后命令行直接输入python，打开python解释器，如图：
![](http://i.imgur.com/mLTIuJy.png)
>说明：因为当前没有linux环境，就使用cywin演示了一下，效果是跟linux的一样的。


### Windows下Python环境搭建
Windows下安装很方便，根据系统版本可下载相对应的Python MSI的安装包，按照步骤点击下一步，即可，默认安装在c:\Python2.x目录，不建议更改它的安装目录。
>注意：在安装的过程最好勾选path那个选项，这样Python在安装完毕会自动建立系统环境变量，这样直接通过cmd窗口就可以输入python，打开Python解释器。

安装完毕通过cmd窗口打开python，如图：
![](http://i.imgur.com/lJ3l2dQ.png)

## Python的文件类型
- 源代码：Python的源代码文件以"py"为扩展名，由Python程序解释，不需要编译，可直接运行，特点：可直接运行，方便修改源代码
- 字节代码：Python源文件经过编译后生成的扩展名为"pyc"的文件，特点：运行速度快
  编译方法：
     ```python
        import py_compile
        py_compile("hello.py")
     ```
- 优化代码：经过优化后的源文件扩展名为".pyo"，特点：运行速度快
  优化方法：
   ```python
        python -O -m py_compile hello.py
   ```
- 以上三种均可以直接运行

## Python变量
变量就是给数据起一个名字，写过shell脚本的，应该知道其中的变量，跟他类似。
变量是计算机内存中的一块区域，变量可以存储规定范围内的值，而且值可以改变。
### 变量的命名：
- 变量名可由字母、数字、下划线组成
- 数字不能开头
- 不可以使用关键字

### 变量的赋值：
  - 是变量声明和定义的过程

### 实例演示：
   ```python
      >>>a = 1
      >>>a
      1
   ```
  >说明：给变量a赋值为1，并显示变量a的赋值结果，相当于我有个同学叫1，但是我先麻烦，所以我就给他另起了一个名称a，这样我直接叫a就可以了，当然叫1也行。变量赋值中间的等号严格意义上需要前后有空格，当然没有空格也行，推荐加空格。

### 设定变量的好处：
方便在脚本或者程序中，简化数据长度或者便于一次性修改脚本或者程序中多次使用的值。
  举个简单的例子，如下：
   ```python
      # coding=utf-8
      #!/bin/bash/env python
      #设定变量a并赋值为50
      a = 50
      
      print "我买本Python学习书籍价格"， a
      print "我喝的可乐价格"， a
      print "我买的车价格是"，  a
   ```
  在上述的脚本中，如果价格发生变化，你是不是得每行去修改，如果内容多，那是不是更麻烦，为了减少这种不必要的操作浪费时间，就在开头设定变量a，然后赋值价格，这样，如果价格发生变化我们只需要修改变量a的值即可。简化数据这个有点跟这个相似，就是如果值的的数据很长，这样会增加代码的可读性难度，设定变量就容易多了。
## 运算符和表达式
### 赋值运算符：
- 赋值运算符符号：`=`
- 最常见的就是对于变量赋值，如： a = 1

### 算数运算符：
算术运算符的优先级跟往常的算数运算符优先级一样，遇到其他特殊的网上再查下，后面再整理。
- 加法： `+`,例如： x+y
- 加等于: `+=`,例如：x += 2相当于x = x+2
- 减法： `-`,例如： x -y
- 减等于: `-=`,例如：x -= 2相当于x = x-2
- 乘法： `*`,例如： x*y
- 乘等于: `*=`,例如：x *= 2相当于x = x*2
- 实数除法： `/`,例如： 3/2,3.0/2
- 整除法： `//`,例如： 5.6/2，5.6//2
- 除等于: `/=`,例如：x /= 2相当于x = x/2
- 求余数： `%`,例如： 17%8余1
- 求余等于： `%=`，例如：x %= 2相当于x = x%2
- 求幂运算: `**`,例如： 2**3 = 8

 >注意：使用除法的时候默认是整除，如果想带小数点，后面必须添加小数点（例如：3.0/2）运算符号只适合在数值中使用，如果放在字符串中就另有其意，后面遇到再说。

### 关系运算符：
- 小于号： `<`,例如： 1 < 2
- 大于号： `>`,例如： 2 > 1
- 小于等于号： `<=`,例如： 1 <= 1,1小于等于1
- 大于等于号： `>=`,例如： 2 >= 2,2大于等于2
- 不等于号： `!=`,例如： 1 != 2，1不等于2
- 完全等于号： `==`,例如： 2 == 2，2等于2

 >注意：运算符号前后建议留出一个空格。

### 逻辑运算符：
- 逻辑与： `and`，例如：1 and 2，判断结果必须同时满足1和2，否则不成立
  - 举个小例子：
     ```python
        # coding=utf-8
        #!/bin/bash/env python

        if 1 == 1 and 1 < 2 :
           print "OK"
        else:
        print "Failed"
    ```
  - 运行上面的脚本，返回值如下：
    ![](http://i.imgur.com/tBczrzR.png)
  - 将上面的1 < 2改为 1 == 2，再次运行脚本，返回值如下：
     ![](http://i.imgur.com/xqCbw3x.png)
  >通过以上实例得知逻辑与（and）必须同时满足and前后两个条件，才会成立，否则不成立。
- 逻辑或： `or`,例如：1 or 2，判断结果只要满足其中一个就成立
  - 将上面例子中的脚本的and改为or：
     ```python
        # coding=utf-8
        #!/bin/bash/env python

        if 1 == 1 or 1 == 2 :
           print "OK"
        else:
        print "Failed"
    ```
  - 再次运行一下，返回值如下：
    ![](http://i.imgur.com/d9aCpAm.png)
  >通过以上实例得知逻辑或（or）只要满足其中一个条件即可成立。
- 逻辑非： `not`,例如： not 0，非0，取反
  - 在上面例子中的脚本的or 后面再添加一个逻辑非（not）：
     ```python
        # coding=utf-8
        #!/bin/bash/env python

        if 1 == 1 and  not 1 == 2 :
           print "OK"
        else:
        print "Failed"
    ```
  - 运行返回结果如下：
     ![](http://i.imgur.com/d9aCpAm.png)
  >在未添加逻辑非（not）时，这个条件是不成立的，因为1不会等于2的，添加逻辑非（not）后，告诉1就是不等于2，所以判断成立，返回OK。

### 表达式：
是将不同数据（包括变量、函数）用运算符号按照一定规则连接起来的一种方式。
- 加号表达式： `+`，用于字符串拼接
  - 如下分别定义一个变量a = "Hello"，b = "World"，想让Hello和World变成一句话，可以使用`+`进行拼接：
     ```python
        >>> a = "Hello"
        >>> b = "World"
        >>> a+b
        'HelloWorld'
    ```
- 乘号表达式：`*`，用于字符串重复出现，`*`后面跟重复的次数
  - 如下定义一个变量a = "Hello"，我想让它重复5次，可以使用a*5，如下：
     ```python
        >>> a = "Hello"
        >>> a*5
        'HelloHelloHelloHelloHello'
    ```
    >注意：使用运算符号作为表达式，进行拼接或者重复出现时，变量的赋值必须是字符串（也就是等号后面的值必须用双引号`""`或者单引号`''`包起来）

## Python数据类型

### 数字
#### 整型
- 整型`int`表示的范围-2，147，483，648到2，147，483，648
  - 例如：1，100，200，-100，-200
- 实例演示，通过给num赋值123，可以通过`type()`查看当前变量的属性：
    ```python
      >>> num=123
      >>> type(num)
      <type 'int'>
    ```

#### 长整型
- 长整型（long）的范围很大，几乎可以说任意大的整数都可以存储，当定义的数值超过整型（int）的范围时，就会使用长整型（long）
- 为了区分普通整型和长整型，需要在整数的后面加大写`L`或者小写`l`
  - 例如：5145677888L, -0x45677532L,建议使用大写`L`，避免数字1与小写`l`混合，造成不必要的麻烦
- 实例演示,定义给一个变量num赋值1L，可以通过type()查看当前变量的属性：
    ```python
      >>> num=1L
      >>> type(num)
      <type 'long'>
    ```
  也可以直接给num赋值一个超过整型(int)范围的数值：
    ```python
      >>> num=99999999999999999999999999999999999999999
      >>> type(num)
      <type 'long'>
    ```
#### 浮点型
- 浮点型（float）也就是常说的小数点类型，例如：3.7.-1.8. 3e+8等等
- 实例演示，通过定义变量num赋值2.3，可以通过type()查看当前变量的属性：
    ```python
      >>> num=1.2
      >>> type(num)
      <type 'float'>
    ```

#### 复数型
- Python对复数（complex）提供内嵌支持，这是其他大部分软件所没有的,使用抛物线经常用到
- 复数类型（complex）通过给数值后面添加`j`来实现，如：3.4j,5.67j,32e-56j
- 实例演示，通过定义变量num赋值2.3j，可以通过type()查看当前变量的属性：
    ```python
       >>> num=1.2j
       >>> type(num)
       <type 'complex'>
    ```

### 字符串
- 使用引号（双引号`""`或者单引号`''`)定义的一组可以包含数字，字母，符号（非特殊符号）的集合
  - 例如：
      ```python
        Name = 'My name is Tom'
        Pay = "This is pay"
        Car = """this is a car"""
      ```
    >- 三重引号（docstring)`""" """`通常用来制作字符串后面再详说。
    >- 如果字符串中存在单引号`''`时可以使用双引号`""``，或者通过转义符`\`来进行转义

## 序列
- 列表、元组和字符串都是序列
- 序列的两个主要特点：索引操作和贴片操作符
  - 索引操作符让我们可以从哪个序列中抓取一个特定的项目
  - 切片操作符让我嫩能够获取序列的一个切片，即一部分序列

### 索引
- 索引操作符是序列后跟一个方括号`[]`，方括号中有一对可选的数字
- 索引同样可是负数，位置是从序列尾部开始计算的
  - 例如，当我们想取出a="12345678"中的8，可以这样做：
      ```python
          >>> a = "12345678"
          >>> a[7]
          '8'
     ```
  - 因为索引可以是负数，也可以这样取值：
       ```python
         >>> a[-1]
         '8'
      ```
    >索引位置从左往右是：01234567，从右往左就是：-1，-2，-3，-4，-5，-6，-7，0

>例如：shop[-1]便是序列的最后一个元素，而shop[-2]抓取到的是序列的倒数第二个元素

### 切片
- 切片操作符是序列后跟一个方括号`[]`，方括号中有一对可选的数字，并用冒号分割
  - 这与索引操作符很相似，不过需要使用`:`，并却是必须的
  - 切片操作符中的第一个数（冒号`:`之前）表示切片开始的位置，第二个数（冒号`:`之后）表示切片到哪里结束（不包含这个位置的元素）。如果不指定第一个数，Python就从序列的首位开始。如果没有指定第二个数，Python则会停止在序列的尾部。
    - 例如，定义变量a赋值字符串'12345678'，然后切取23456：
        ```python
          >>> a = "12345678"
          >>> a[1:6]
          '23456'
       ```
      >说明：计算机中`0`是默认开始位置，所以上述12345678对应的位置就是01234567，当我们要切取23456的字符串时，就得从1开始，按照切片取值定义想取到字符串6就得定位到6（这里的6不是字符串6，是7的位置）
    - 从位置1开始取值，不指定第二个位置，将会取到2345678：
         ```python
          >>> a = "12345678"
          >>> a[1:]
          '2345678'
         ```
    - 如果只有`[:]`将会打印出所有的值：
        ```python
          >>> a = "12345678" 
          >>> a[:]
          '12345678'
       ```
    - 当出现`[::]`时，后面没有步长值，默认位置为1，打印效果：
       ```python
         >>> a = "12345678" 
         >>> a[:：]
         '12345678'
       ```
    - 当`[::]`里面设定步长值后，如设置步长值为2：[::2]，打印效果：
       ```python
        >>> a = "12345678" 
        >>> a[:：2]
        '1357'
       ```
      >`[::2]`其实就是起到步长值得作用，后面的数字2就是走两步取后面一个值，上述的例子中，从位置1开始取值，然后从1位置走两步（也就是到位置3）取后面值3，然后从位置3走两步（也就是位置5）取后面值5，然后从位置5走两步（也就是位置7）取后面值7，最后取出来为1357.这里所说的走2步就是从位置1开始走到位置2算一步，然后到位置3就是第二步。

### 序列的基本操作
- `len()`:求序列长度
  - 例如求a = "12345678"的长度：
      ```python
        >>>a = "12345678"
        >>> len(a)
        8
      ```
- `+`:连接2个序列：
   - 例如：
       ```python
         >>> a = "Hello"
         >>> b = "World"
         >>> a + b
         'HelloWorld'
      ```
- `*`:重复序列：
  - 例如将hello重复5次：
       ```python
         >>> a = "Hello"
         >>> a*5
         'HelloHelloHelloHelloHello'
      ```
- `in`：判断元素是否在序列中
   - 例如判断c是否在a = "Hello"中：
       ```python
         >>> a = "Hello"
         >>> 'c' in a
         False
      ```
     >返回Fasle说明不存在
- `max()`:返回最大值
   - 例如查看a = "12345678"中的最大值：
       ```python
         >>> a = "12345678"
         >>> max(a)
         '8'
       ```
- `min()`:返回最小值
   - 例如查看a = "12345678"中的最小值：
       ```python
         >>> a = "12345678"
         >>> min(a)
         '1'
       ```
- `cmp(tuple1, tuple2)`:比较2个序列的值是否相等
   - 例如判断a = "3"与b = "4",返回结果：
       ```python
         >>> a = "3"
         >>> b = "4"
         >>> cmp(a, b)
         -1
       ```
   - 如果a与b换个位置在进行比较一下看下返回结果：
       ```python
         >>> cmp(b, a)
         1
       ```
   - 如果a和b的值相等，看下返回值：
        ```python
         >>> a = "3"
         >>> b = "3"
         >>> cmp(b, a)
         0
       ```
   >通过以上例子可以看出，当使用`cmp（tuple1，tuple2）`进行比较的时候，如果前面的数值大于后面的会返回1，小于时会返回-1，等于时会返回0，另外如果字符串是字母的时候它一般会按照英文字母的顺序进行比对，通常是后面的字母大于前面的，如：

    ```python  
      >>> a = "c"
      >>> b = "d"
      >>> cmp(b, a)
      1
    ```
   
### 元组
- 元组和列表十分相似，只不过元组和字符串一样是不可变得，即你不能修改元组
- 元组通过圆括号`()`和其中的逗号`,`来分割项目，例如：（1，2，3，4）
- 元组通常用在使语句和用户定义的函数能够安全的采用一组固定（这里的固定式说这组的值不能随意更改）的值得时候使用。
- 定义元组可以包含字符串、列表、数字等，通过逗号`,`分隔。
- 元组的好处，定义范围广
- 元组是不可变类型的数据
- 创建元组:
  - 一个空元组由一对空的圆括号`( )`组成，例如： a = ()
  - 含有单个元素的元组，如：
    - a = (2`,`)
    >注意：定义一个单个元组，元素后面必须有一个逗号`,`这个比较特殊一些。

  - 一般元组, 如：
    -  name = ('Tom','Joy','jack')
    -  user_pay = ('Tom','egg',20)
  - 可以通过type()函数来当前变量的属性：
     ```python
      >>> a = (2,)
      >>> type(a)
      <type 'tuple'>
     ```
    >- 看到tuple就说明此变量为元组
- 元组操作：
  - 元组和字符串类型一样都是属于序列类型，可以通过索引和切片操作
  - 定义好的元组，值不能改变
- 实例演示，定义一个元组a = ('Tom',30,'male')
  - 试图更改元组里面的元素，这里试图修改一个值：
     ```python
      >>> a = ('Tom',30,'male')
      >>> a[1] = 31
      Traceback (most recent call last):
        File "<stdin>", line 1, in <module>
      TypeError: 'tuple' object does not support item assignment
     ```
     >修改其中一个元素报错：告诉我们元组是不支持组分配指定的，也就说不能修改。
  - 拆分元组操作：
     ```python
     >>> a = ('Tom',30,'male')
     >>> name
     'Tom'
     >>> age
     30
     >>> sex
     'male'
     >>> name,age,sex
     ('Tom', 30, 'male')
     ```
### 列表
- 列表(List)是处理一组有序项目的数据结构，即你可以在一个列表中存储一个序列的项目
- 列表是可变类型的数据
- 列表跟元组一样，定义范围广，元素可以是字符串、数字，其中也可以有列表和元组，不过元组不能修改
- 列表的组成：用方括号`[]`表示列表，包含多个元素以逗号`,`分隔，如：
  - List1 = ['Tom','列表',1]
  - List2 = [1,2,3,4,5]
  - List3 = ["python","Linux","wiondows"]
  - List4 = [1]
    >列表不像元组，单个元素的的列表后面需要添加逗号`,`
  - 以上实例可以通过`type()`函数查看器属性，返回结果如下：
       ```python
       >>> List1 = ['Tom','列表',1]
       >>> type(List1)
       <type 'list'>
       ```
       ```python
       >>> List2 = [1,2,3,4,5]
       >>> type(List2)
       <type 'list'>
       ```
       ```python
       >>> List3 = ["python","Linux","wiondows"]
       >>> type(List3)
       <type 'list'>
       ```
       ```python
       >>> List4 = [1]
       >>> type(List4)
       <type 'list'>
       ```
- 列表操作方法：
  - 取值：
    - 索引取值：
      定义一个列表：a = [1,2,3,4,5],通过索引取值：
      ```python
       >>> a = [1,2,3,4,5]
       >>> a[0]
       1
       >>> a[1]
       2
       >>> a[4]
       5
      ```
    - 切片取值：
      定义一个列表：a = [1,2,3,4,5],通过切片取值：
      - 从位置1开始取值，到列表位置结束：
        ```python
          >>> a = [1,2,3,4,5]
          >>> a[1:]
         [2, 3, 4, 5]
        ```
     - 从位置1取值，到位置4：
       ```python
        >>> a = [1,2,3,4,5]
        >>> a[1:4]
        [2, 3, 4]
       ```
     - 从位置4结束取值:
       ```python
        >>> a = [1,2,3,4,5]
        >>> a[:4]
        [1, 2, 3, 4]
       ```
     - 使用`[::]`设定步长值取值，此处设定步长值为2：
       ```python
        >>> a = [1,2,3,4,5]
        >>> a[::2]
        [1, 3, 5]
       ``` 
       >说明：从位置1开始取值（设定步长值后，起始位置为1），然后走2步到位置3取值3（位置3的值），然后从位置3开始走2步取值5（位置5的值），这里所说的走2步就是从位置1开始走到位置2算一步，然后到位置3就是第二步。
    - 添加值，使用属性`append`来实现：
      - 定义一个列表a = [1,2,3,4,5],然后通过`append`属性添加值：
        ```python
         >>> a = [1,2,3,4,5]
         >>> a.append(6)
         >>> a
         [1, 2, 3, 4, 5, 6]
        ```
       >说明：属性`append`属于给列表结尾追加值，存储空间会变化，可通过`id`来确认
    - 删除值：
      - 使用`del`删除列表中的元素：
        ```python
         >>> a = [1,2,3,4,5,6]
         >>> del(a[5])
         >>> a
         [1, 2, 3, 4, 5]
        ```
        >`del()`通过列表索引删除指定的元素，好处在于如果列表元素太长，使用`del()`能快速删除指定的元素，简单明了。而且可以直接删除整个列表。
     - 使用`remove`删除列表中的元素：
        ```python
         >>> a = [1,2,3,4,5]
         >>> a.remove(5)
         >>> a
         [1, 2, 3, 4]
        ```
       >`remove`直接指定列表的元素就可以删除
     
    - 修改值：
      - 通过`list[] = x`来对列表中的元素进行修改：
        ```python
         >>> a = [1,2,3,4]
         >>> a[3] = 5
         >>> a
         [1, 2, 3, 5]
        ```
       >通过索引重新赋值即可
   - 修改列表中的元素列表的存储空间不变（扩展说明），例：
      - 定义一个列表a = [1,2,3,4,5]
      - 首先查看列表a的存储空间id:
        ```python
         >>> a = [1,2,3,4,5]
         >>> id(a)
         7696579682248
        ```
      - 通过索引重新赋值修改其中一个元素的值：
        ```python
        >>> a = [1,2,3,4,5]
        >>> a[1] = 6
        >>> a
        [1, 6, 3, 4, 5]
        ```
     - 再次通过`id()`来查看列表a的存储空间id值：
       ```python
       >>> a = [1,6,3,4,5]
       >>> id(a)
       7696579682248
       ```
       >此时发现修改列表a的值后，通过`id()`查看存储空间id，未变化
    - 查找值：
      - 通过`var in list`来查找列表中是否有这个值：
        ```Python
        >>> a = [1,2,3,5]
        >>> a in a
        False
        >>> 5 in a
        True
        ```
       >说明：在列表中查找a，a不存在返回`False`，查找5存在则返回`True`
       
### 字典
- 字典是python中唯一的映射类型`{哈希表}`
- 字典对象是可变的，但是字典的键必须使用不可变对象，并且一个字典中可以使用不同类型的键值
- `keys()`或者`values()·返回列表或者值列表
- `items()`返回包含键值对的元组
- 创建字典：
  - 使用花括号`{}`,例如： a = {0:'id',1:'name',2:age'}，执行结果：
    ```python
    >>> a = {0:'id',1:'name',2:'age'}
    >>> a
    {0: 'id', 1: 'name', 2: 'age'}
    ```
  - 使用工厂方法`dict()`，这种方法慢，例如：fdict = dict((['x',1],['y',2])),执行结果：
    ```python
    >>> fdict = dict((['x',1],['y',2]))
    >>> fdict
    {'y': 2, 'x': 1}
    ```
    >注意：`dict()`圆括号里面是映射对象的`(key,value)对`中初始化新字典
    当然了也可以在关键列表中使用`name=value对`初始化新字典，例如：a = dict(one=1,two=2),执行结果如下：
    ```python
    >>> a = dict(one=1,two=2)
    >>> a
    {'two': 2, 'one': 1}
    ```
    
  - 内建方法：`fromkeys()`,字典中的元素具有相同的值，默认为None，例如：num = {}.fromkeys(('x','y'),-1),执行结果：
    ```python
    >>> num = {}.fromkeys(('x','y'),-1)
    >>> num
    {'y': -1, 'x': -1}
    ```
- 访问字典中的值：
  - 直接使用`key`：`key`不存在会报错，可以使用`has_key()`或者`in`和`not in`判断，`has_key()`方法即将被弃用,如判断字典 a =  {'age': 23, 'name': 'guo', 'sex': 'm'}中是否存在键值name，执行结果如下：
     ```python
     >>> a.has_key('name')
     True
     ```
     当然了也可以通过`in`和`not in`判断，判断键值name和aa是否存在在字典a中，执行结果如下：
     ```python
     >>> 'name' in a
     True
     >>> 'aa' not in a
     True
     ```
     >说明：返回值为`True`代表存在，`Fasle`代表不存在
  - 循环遍历,；例如：
     ```python
     for key in dict1.keys():
     ```
    实例：
     ```python
       >>> a = {'name':'guo','age':23,'sex':'m'}
       >>> a
       {'age': 23, 'name': 'guo', 'sex': 'm'}
       >>> a = {'name':'guo','age':23,'sex':'m'}
       >>> a
       {'age': 23, 'name': 'guo', 'sex': 'm'}
     ```
    打印key值：
      ```python
       >>> for key in a:
       ...     print key
       ...
       age
       name
       sex
       ```
       打印value值：
       ```python
       >>> for key in a:
       ...     a[key]
       ...
       23
       'guo'
       'm'
      ```
  - 使用迭代器，例如：
      ```python
       for key in dict1:
      ```
- 更新和删除：
  - 直接使用键值访问更新，内建的`update()`方法可以将整个字典的内容拷贝到另一个字典中，例如将字典b = {'room': 1, 'service': 220, 'number': 202}拷贝到字典a = {'age': 23, 'name': 'guo', 'sex': 'm'}中，执行结果如下：
    ```python
     >>> a = {'age': 23, 'name': 'guo', 'sex': 'm'}
     >>> b = {'room': 1, 'service': 220, 'number': 202}
     >>> a.update(b)
     >>> a
     {'name': 'guo', 'service': 220, 'room': 1, 'age': 23, 'number': 202, 'sex': 'm'}
    ```
    >说明：字典当中是无序排列，所以不管你添加还是修改，最后的输出都会与之前的序列不一致
  - `del dict1['a']`删除字典中键值为a的元素，例如删除字典d = {'car':'baoma','color':'blue'}中的color键和对应的值，执行结果如下：
      ```python
        >>> d = {'car':'baoma','color':'blue'}
        >>> d
        {'color': 'blue', 'car': 'baoma'}
        >>> del d['color']
        >>> d
        {'car': 'baoma'}
      ```
    - `dict11.pop('a')`删除并返回键为'a'的元素，例如删除字典a = {'car': 'baoma'},执行结果如下：
       ```python
         >>> a = {'car': 'baoma'}
         >>> d.pop('car')
         'baoma'
         >>> d
         {}
      ```
     >说明：字典内建方法`dict.pop()`与其他内建`pop()`有区别的，具体需要查看help手册(`help(object.pop))`
    - `dict1.clear()`删除字典所有的元素,例如删除字典d = {'car':'baoma','color':'blue'}中所有的元素，执行结果如下：
        ```python
         >>> d = {'car':'baoma','color':'blue'}
         >>> d
         {'color': 'blue', 'car': 'baoma'}
         >>> d.clear()
         >>> d
         {}
        ```  
    - `del dict1`删除整个字典，例如删除字典d = {'car':'baoma','color':'blue'}，执行结果如下：
        ```python
         >>> d = {'car':'baoma','color':'blue'}
         >>> d
         {'color': 'blue', 'car': 'baoma'}
         >>> del d
         >>> d
         Traceback (most recent call last):
           File "<stdin>", line 1, in <module>
         NameError: name 'd' is not defined
     ```
     >说明：底下报错d没有被定义，说明字典d已经不存在了
  - `dict1['a] = 'string'`添加一对键值，例如给c = {'id':1,'class':23,'location':345}添加一对键值'pay':45，执行结果如下：
    ```python
     >>> c = {'id':1,'class':23,'location':345}
     >>> c['pay'] = 45
     >>> c
     {'pay': 45, 'location': 345, 'id': 1, 'class': 23}
    ```
- 字典相关的内建函数：
  - `type()`、`str()`、`cmp()`（cmp很少用于字典比较，
比较依次是字典的大小、键、值）。
  - 工厂函数`dict()`，例如：a = dict((['x','y'],[1,2]))，b = (one=1,two=2),执行结果如下：
     ```python
       >>> a = dict((['x','y'],[1,2]))
       >>> a
       {'x': 'y', 1: 2}
     ```
     ```python
       >>> b = dict(one=1,two=2)
       >>> b
       {'two': 2, 'one': 1}
     ```
  - 使用`dict()`生成字典比用`copy慢，因此这种情况下推荐使用`copy()`，例如：将字典 t = {'x':1,'y':2}的元素拷贝给新的字典c，使其拥有字典t一样的键值，执行结果如下：
    ```python
    >>> t = {'x':1,'y':2}
    >>> c = t.copy()
    >>> c
    {'y': 2, 'x': 1}
    ```
   >说明：`copy()`属于字典内建函数，所以直接使用`help(copy)`是无法查看其帮助信息的，应该是`help(t.copy)`才能查看其帮助信息，这个与python中`import copy`有区别的，虽然用法差不多一样，简单说，查看字典内建函数的帮助信息用法`help(t.copy)`其中的`t`是字典的对象，`copy`是其内建方法（也就是内建函数）
   
    - 具体事例如下，首先得创建一个字典，如：a = {'x':1,'y':2}
    - 先查看字典`a`对象的所有的帮助信息，执行以下步骤：
      ```python
       >>> help(a)
       Help on dict object:
       
       class dict(object)
      |  dict() -> new empty dictionary
      |  dict(mapping) -> new dictionary initialized from a mapping object's
      |      (key, value) pairs
      |  dict(iterable) -> new dictionary initialized as if via:
      |      d = {}
      |      for k, v in iterable:
      |          d[k] = v
      |  dict(**kwargs) -> new dictionary initialized with the name=value pairs
      |      in the keyword argument list.  For example:  dict(one=1, two=2)
      |
      |  Methods defined here:
      |
      |  __cmp__(...)
      |      x.__cmp__(y) <==> cmp(x,y)
      |
      |  __contains__(...)
      |      D.__contains__(k) -> True if D has a key k, else False
      |
      |  __delitem__(...)
      |      x.__delitem__(y) <==> del x[y]
      
      ......
      
      |  clear(...)
      |      D.clear() -> None.  Remove all items from D.
      |
      |  copy(...)
      |      D.copy() -> a shallow copy of D
      |
      |  fromkeys(...)
      |      dict.fromkeys(S[,v]) -> New dict with keys from S and values equal to v.
      |      v defaults to None.
      ```
      >说明：这就显示当前字典`a`所有的类和方法的帮助信息
    
   - 查看字典中`copy()`的帮助信息，执行一下步骤：
     ```python
       >>> help(a.copy)
       Help on built-in function copy:
	  
       copy(...)
           D.copy() -> a shallow copy of D
       (END)
     ```
    >说明：这里面就是字典内建函数`copy()`的查看帮助信息，其他的也是这样弄得，执行命令就得`字典对象.内建函数()`,例：`a.copy()`
- 字典内建函数方法小结：
  - `len()`，输出字典长度，其实也是系统内建函数,列表、元组变量都能使用，使用方法：`len(object)`，例如：
    ```python
    >>> a = {'x':1,'y':2}
    >>>  len(a)
    2
    ```
    >说明：`len()`输出的长度在字典中是按一对键值来输出的，在列表、元组】变量中是按照里面的元素计算输出的，也就是说一对键值就是一个长度
  - `hash`,系统内建函数，用于判断某个对象是否可以做一个字典的建，非哈希类型的报TypeError错误，使用方法`hash(object)`,例如：
    ```python
    >>> a = {'x':1,'y':2}
    >>> hash(a)
    Traceback (most recent call last):
      File "<stdin>", line 1, in <module>
    TypeError: unhashable type: 'dict'
    ```
    ```python
    >>> a = {'x':1,'y':2}
    >>> hash(3)
    3
    ```
    >备注简单说只要hash的对象结果有返回值，并且不报错就可以最为一个字典的键值使用，`hash(object)`也可用配合关系运算符判断两个对象是否相等（对于两对象使用这个，感觉有点多次一举，具体的后面研究了再说把）
  - `dict.has_key(key)`判断字典中是否存在key（建议使用`in`和`not in`代替）,他属于字典内建函数方法，使用方法：
    ```python
    >>> a = {'x':1,'y':2}
    >>> a.has_key(2)
    False
    >>> a.has_key('x')
    True
    >>> a.has_key('y')
    True
    ```
    >备注：其实这个前面已经说过的，这个后续会摈弃这个方法的
  - `dict.items()`返回键值对元组的列表，属于字典内建函数方法，例如：
     ```python
     >>> a = {'x':1,'y':2}
     >>> a.items()
     [('y', 2), ('x', 1)]
     ```
     >说明：也就是说将字典里面的键值对组成元组，最后以一个列表的形式输出
  - `dict.iter*()`（里面的星号代表后面有个方法名称），返回迭代子而不是列表，使用方法：
    - `dict.iteritems()`：
       ```python
       >>> a = {'x':1,'y':2}
       >>> a.iteritems()
       <dictionary-itemiterator object at 0x6ffffbb8f70>
      ```     
    - `dict.iterkeys()`:
       ```python
       >>> a = {'x':1,'y':2}
       >>> a.iterkeys()
       <dictionary-keyiterator object at 0x6ffffbb8fc8>
       ```
    - `dict.itervalues()`:
       ```python
       >>> a = {'x':1,'y':2}
       >>> a.itervalues()
       <dictionary-valueiterator object at 0x6ffffbb8f70>
       ```
      >备注：这个有点高大上了，这个迭代子目前不知道具体是干嘛用的，
  - `dict.get(key[,default=none])`,返回key的值，如果不存在返回default指定的值（命令中帮助参数中的`[]`代表可选，可有可无），这里的default指定是说当key不存在的时候，你可以任意指定一个返回值，例如：
    ```python
    >>> a = {'x':1,'y':2}
    >>> a.get('x')
    1
    >>> a.get('z', 'z is not exist')
    'z is not exist'
    ```
    >说明：第一次get x键值，因为存在，所以返回x键的值1，第二次get z，不存在，默认是返回none，也就是返回结果不会有任何提示，为了友好点，我们就指定一个不存在的提示语，执行后悔看到我们指定的提示语：'z is not exist'
  - 其他字典内建的函数方法，就不再说了，可以使用`help(object)`（这里的object就是字典的对象，如：a = {'x':1,'y':2}，对象就是a）查看所有的类和方法，英文的不明白，推荐去[RUNOOB.COM](http://www.runoob.com/python/python-tutorial.html)看下，这里讲的可比我总结的详细，我这是自己学习总结为了加深学习记忆而已。

## 流程控制
- `if`语句：
  - Python的`if`语句类似于其他语言，`if`语句包含一个逻辑表达式，使用表达式比较，在比较的结果的基础上做出决定。
  - 语法格式：
    ```python
    if expression: 如果表达式(等于、不等于、大于、小于、存在、不存在等)满足条件
        statement(s) 声明（执行代码或者显示需要显示的结果)
    ```
    >说明：Python语言使用缩进作为其语句（代码块）分组的方法，建议使用4个空格代替其他缩进格式（这也是官方推荐的，主要是为了兼容跨平台），缩进相同的被认为是一个代码块。
  - 实例，判断1>2：如下：
    ```python
    >>> if 1 < 2:
    ...     print "1 小于 2正确"
    ...
    1 小于 2正确
    ```
    >注意：python当中的`if`语句跟其他语言的格式可能有点区别的，比如shell当中是这样的：
    ```python
    if expression;
    then
        statement(s)
    fi
    ```
- `if`语句常用的逻辑值表达式（bool）：
  - 逻辑值（bool）用来表示诸如：对与错、真与假、空与非空等概念
  - 逻辑值包含了两个值：
    - True：表示非空的量（string，tuple，list，set，dictonary等），所有非空零数
    - False：表示0，None，空的量等
  - 作用：主要用在判断语句中进行判断：
    - 一个字符串是否空的
    - 一个运算是否为零
    - 一个表达式是否可用

   >说明：True就是真实存在的，比如：判断1<2，本来1肯定小于2，所以结果肯定是True了，False就是不存在，例如：1>2，根本不可能的，所以结果是False
  - 实例：
    - 判断条件为True，查看返回结果：
       ```python
        # vi python.py
        #!/bin/env python
	    
        if True:
            print "True is ok"
        print "Fasle and True"
       ```
       ```python
        # python python.py
        True is ok
        Fasle and True
      ```
      >备注：当条件为True时，所有的print都返回,这里写在3脚本是为直观
   - 判断条件为False，查看返回结果：
      ```python
       # vi python
       #!/bin/env python
	   
        if True:
            print "True is ok"
        print "Fasle and True"
     ```
     ```python
      # python python
      Fasle and True
     ```
     >备注：此时，当条件为`False`时，返回结果只`print "Fasle and True"`，之所以这里还会仍旧显示这个，是因为`print "Fasle and True"`跟`if`同级别的，不在`if`的判断里面
- else语句：
  - else语句不能单独使用，必须配合if使用
  - 语法格式：
    ```python
    if expression:   如果表达式成立
        statement(s) 执行代码
    else:            否则 
        statement(s) 执行这个代码
    ```
   >备注：`else`是个可选的语句，并且一个`if`语句中只能使用一个`else`语句
  - 实例：
    判断如果用户输入一个数字1返回ok，否则返回error：
    ```python
     # cat p.py
     #!/bin/env python
     
     a = raw_input("please input number: ")
     
     if a == "1":
         print "your input is ok"
     else:
         print "your input is Error"
    ```
    ```python
     # python p.py
     please input number: 1
     your input is ok
    ```
    ```python
     # python p.py
      please input number: 2
      your input is ok 
    ```
- `elif`语句：
  - `elif`语句存在的意义，当需要多个表达式为真值时执行一段代码，`elif`可以存在多个，并且它也是可选的，比如说,当用户输入1-5的数字时，执行一段代码告诉他相对应的结果，否则就告诉他失败
  - 语法格式：
    ```python
    if expression:     如果满足条件
        statement(s)   执行这个代码
    elif expression2:  如果也满足这个条件
        statement(s)   执行这个代码
    elif expression3:
        statement(s)
    ......
    else:              否则
        statement(s)   执行这个代码
    ```  
  - 实例：：
    判断如果用户输入1-5就返回相应的结果，否则就返回error：
    ```python
    # vi p.py
    #!/bin/env python

    a = int(raw_input("pleae your number: "))
    
    if a == 1:
        print "your input number is 1 ok"
    elif a == 2:
        print "your input number is 2 ok"
    elif a == 3:
        print "your input number is 3 ok"
    elif a == 4:
        print "your input number is 4 ok"
    elif a == 5:
        print "your input number is 5 ok"
    else:
        print "your input number is %s error" % a
    ```
   
    ```python
    # python p.py
    pleae your number: 1
    your input number is 1 ok
    ```
    ```python
    # python p.py
    pleae your number: 6
    your input number is 6 error
    ```
     >备注：就演示一下输入1和输入6就可以达到目的了,这里面的`%s`和`%`输出格式化的字符串和格式化字符串



