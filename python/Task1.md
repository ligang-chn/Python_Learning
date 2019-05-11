

### Task1

##### 1、Python环境搭建

###### （1）资源池

​	**python安装包（建议）**：Anaconda（支持多种操作系统，集成了主流的科学计算包）

​	下载链接：

​	官网： <https://www.continuum.io/downloads>

​	清华大学镜像：<https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/>

​	**python IDE（建议）：**PyCharm （由 JetBrains 打造的一款 Python IDE，支持 macOS、 Windows、 Linux 系统）

​	下载链接：

​	官网：<https://www.jetbrains.com/pycharm/download/#section=windows>



 	**python参考教程和网站：**

- Python编程从入门到实践，Eric Mathes著，人民邮电出版社

- SciPy科学计算生态圈：<https://www.scipy.org/>

- Wes McKinney, Python for Data Analysis. 东南大学出版社（英文影印本，中译版名为《利用Python进行数据分析》）

- 廖雪峰python学习笔记：https://blog.csdn.net/datawhale/article/category/7779959

- python入门笔记

  作者李金，这个是jupyter notebook文件，把python的主要语法演示了一次，值得推荐。下载链接: 

  https://pan.baidu.com/s/1IPZI5rygbIh5R5OuTHajzA 提取码: 2bzh

- 南京大学python视频教程

  这个教程非常值得推荐，python主要语法和常用的库基本涵盖了。

  查看地址：

  https://www.icourse163.org/course/0809NJU004-1001571005?from=study

  

  **安装教程：**

- Anaconda+Jupyter notebook+PyCharm：https://zhuanlan.zhihu.com/p/59027692

- Python入门：Anaconda和PyCharm的安装和配置：<https://www.cnblogs.com/yuxuefeng/articles/9235431.html>

  

###### （2）解释器

​	**1）编译器和解释器的联系**

​	相同点：

- 两者都是高级语言与机器之间的翻译官。
- 都是将代码翻译成可以执行的二进制机器码，只不过在运行原理和翻译过程有不同而已。

​	不同点:

![1557553221597](assets/1557553221597.png)

​	用一个通俗的例子进行比喻：我们去饭馆吃饭，点了八菜一汤。编译器的方式就是厨师把所有的菜给你全做好了，一起给你端上来，至于你在哪吃，怎么吃，随便。解释器的方式就是厨师做好一个菜给你上一个菜，你就吃这个菜，而且必须在饭店里吃。

​	![1557553309484](assets/1557553309484.png)

​	**2）Python解释器种类**

​	Python有好几种版本的解释器：

- **CPython**：官方版本的解释器。这个解释器是用C语言开发的，所以叫CPython。CPython是使用最广的Python解释器。我们通常说的、下载的、讨论的、使用的都是这个解释器。

- **Ipython**：基于CPython之上的一个交互式解释器，在交互方式上有所增强，执行Python代码的功能和CPython是完全一样的。CPython用>>>作为提示符，而IPython用In [序号]:作为提示符。

- **PyPy**：一个追求执行速度的Python解释器。采用JIT技术，对Python代码进行动态编译（注意，不是解释），可以显著提高Python代码的执行速度。绝大部分CPython代码都可以在PyPy下运行，但还是有一些不同的，这就导致相同的Python代码在两种解释器下执行可能会有不同的结果。

- **Jython**：运行在Java平台上的Python解释器，可以直接把Python代码编译成Java字节码执行。

- **IronPython**：和Jython类似，只不过IronPython是运行在微软.Net平台上的Python解释器，可以直接把Python代码编译成.Net的字节码。

  【参考资料】：

  a. 编译器与解释器：<http://www.liujiangblog.com/course/python/9>

  b. 编译器与解释器的异同：<https://blog.csdn.net/zp357252539/article/details/78660131>



###### （3）python运行方式

​	1）Shell方式

​		shell是交互式的解释器，输入一行命令，解释器就解释运行相应结果；

​	2）文件方式

​		在Python的IDE环境中，创建一个以py为扩展名的文件，用Python解释器在Shell中运行结果；

​	

##### 2 、Python语法

###### （1）输入和输出：print&input函数

​	**print函数：**

​		— print（变量）

​		— print （字符串）

​		print函数可以接受多个字符串，用逗号“，”隔开，就可以连成一串输出。



​	**input函数：**返回的类型是字符型；同时，输入是可以带提示语的。

​		![1557554819805](assets/1557554819805.png)

​		***Note：***_如果要求输出的是int、float等类型，需要通过int（）、float（）等函数转换。如下图所示：_

​		![1557555009653](assets/1557555009653.png)

​		_eval（）函数用来执行一个字符串表达式，并返回表达式的值，其语法：_

```
	eval(expression[, globals[, locals]])
```

###### （2）Python风格

​	注释：“#”；

​	续行：“\"；

​		无需换行符可直接换行的两种情况：

​		a. 小括号、中括号、花括号的内部可以多行书写；

​		b. 三引号包括下的字符串也可以跨行书写。

​	一行多语句：”；“

​	缩进：相同的缩进表示同级别的语句块和范围；

###### （3）语法基础

​	**1）变量**













































































































&emsp; **CPython**：官方版本的解释器。这个解释器是用C语言开发的，所以叫CPython。CPython是使用最广的Python解释器。我们通常说的、下载的、讨论的、使用的都是这个解释器。

&emsp;**Ipython**：基于CPython之上的一个交互式解释器，在交互方式上有所增强，执行Python代码的功能和CPython是完全一样的。CPython用>>>作为提示符，而IPython用In [序号]:作为提示符。

**PyPy**：一个追求执行速度的Python解释器。采用JIT技术，对Python代码进行动态编译（注意，不是解释），可以显著提高Python代码的执行速度。绝大部分CPython代码都可以在PyPy下运行，但还是有一些不同的，这就导致相同的Python代码在两种解释器下执行可能会有不同的结果。

**Jython**：运行在Java平台上的Python解释器，可以直接把Python代码编译成Java字节码执行。

**IronPython**：和Jython类似，只不过IronPython是运行在微软.Net平台上的Python解释器，可以直接把Python代码编译成.Net的字节码。