# Python学习笔记

Python提供了高效的高级数据结构，还能简单有效地面向对象编程。Python语法和动态类型，以及解释型语言的本质，使它成为多数平台上写脚本和快速开发应用的编程语言



## 一、优点
**1.简单**：Python是一种代表简单主义思想的语言。阅读一个良好的Python程序就感觉像是在读英语一样。它使你能够专注于解决问题而不是去搞明白语言本身。

**2.易学**：Python极其容易上手，因为Python有极其简单的说明文档。

**3.速度快**：Python 的底层是用 C 语言写的，很多标准库和第三方库也都是用 C 写的，运行速度非常快。

**4.免费、开源**：Python是FLOSS（自由/开放源码软件）之一。使用者可以自由地发布这个软件的拷贝、阅读它的源代码、对它做改动、把它的一部分用于新的自由软件中。FLOSS是基于一个团体分享知识的概念。

**5.高层语言**：用Python语言编写程序的时候无需考虑诸如如何管理你的程序使用的内存一类的底层细节。

**6.可移植性**：由于它的开源本质，Python已经被移植在许多平台上（经过改动使它能够工作在不同平台上）。这些平台包括Linux、Windows、FreeBSD、Macintosh、Solaris、OS/2、Amiga、AROS、AS/400、BeOS、OS/390、z/OS、Palm OS、QNX、VMS、Psion、Acom RISC OS、VxWorks、PlayStation、Sharp Zaurus、Windows CE、PocketPC、Symbian以及Google基于linux开发的android平台。

**7.解释性**：一个用编译性语言比如C或C++写的程序可以从源文件（即C或C++语言）转换到一个你的计算机使用的语言（二进制代码，即0和1）。这个过程通过编译器和不同的标记、选项完成。运行程序的时候，连接/转载器软件把你的程序从硬盘复制到内存中并且运行。而Python语言写的程序不需要编译成二进制代码。你可以直接从源代码运行 程序。在计算机内部，Python解释器把源代码转换成称为字节码的中间形式，然后再把它翻译成计算机使用的机器语言并运行。这使得使用Python更加简单。也使得Python程序更加易于移植。

**8.面向对象**：Python既支持面向过程的编程也支持面向对象的编程。在“面向过程”的语言中，程序是由过程或仅仅是可重用代码的函数构建起来的。在“面向对象”的语言中，程序是由数据和功能组合而成的对象构建起来的。

**9.可扩展性**：如果需要一段关键代码运行得更快或者希望某些算法不公开，可以部分程序用C或C++编写，然后在Python程序中使用它们。

**10.可嵌入性**：可以把Python嵌入C/C++程序，从而向程序用户提供脚本功能。

**11.丰富的库**：Python标准库确实很庞大。它可以帮助处理各种工作，包括正则表达式、文档生成、单元测试、线程、数据库、网页浏览器、CGI、FTP、电子邮件、XML、XML-RPC、HTML、WAV文件、密码系统、GUI（图形用户界面）、Tk和其他与系统有关的操作。这被称作Python的“功能齐全”理念。除了标准库以外，还有许多其他高质量的库，如wxPython、Twisted和Python图像库等等。

**12.规范的代码**：Python采用强制缩进的方式使得代码具有较好可读性。而Python语言写的程序不需要编译成二进制代码。



## 二、缺点

1. **单行语句和命令行输出问题**：很多时候不能将程序连写成一行，如import sys;for i in sys.path:print i。而perl和awk就无此限制，可以较为方便的在shell下完成简单程序，不需要如Python一样，必须将程序写入一个.py文件。
2. **独特的语法**：这也许不应该被称为局限，但是它用缩进来区分语句关系的方式还是给很多初学者带来了困惑。即便是很有经验的Python程序员，也可能陷入陷阱当中。
3. **运行速度慢**：这里是指与C和C++相比。



## 三、应用领域

- Web 和 Internet开发
- 科学计算和统计
- 人工智能
- 桌面界面开发
- 软件开发
- 后端开发
- 网络接口：能方便进行系统维护和管理，Linux下标志性语言之一，是很多系统管理员理想的编程工具。

## Python的主体内容大致可以分为以下几个部分：

1、面向过程，包括基本的表达式，if语句，循环，函数等。如果你有任何一个语言的基础，特别是C语言的基础，这一部分就是分分钟了解下Python规定的事。如果你没有语言基础，建议用Python Programming为参考书。这本书是计算机导论性质的教材，不需要编程基础。

2、面向对象，包括面向对象的基本概念，类，方法，属性，继承等。Python是面向对象的语言，“一切皆对象”。面向对象是很难回避的。Python的面向对象机制是相对比较松散的，不像Java和C++那么严格。好处是容易学，容易维护，坏处是容易犯错。

3、应用功能，包括IO，数据容器如表和词典，内置函数，模块，格式化字符串等。这些在其它语言中也经常出现，有比较强的实用性。

4、高级语法，上下文管理器，列表推导，函数式编程，装饰器，特殊方法等。这些语法并不是必须的，你可以用前面比较基础的语法实现。学这些高级语法的主要原因是：它们太方便了。比如列表推导一行可以做到的事情，用循环结构要好几行才行。

标准库只是调用功能的接口，最终实现的是Python和系统的互动。这需要很强的系统知识，比如文件系统知识，进程管理，http原理，socket编程，数据库原理…… 

