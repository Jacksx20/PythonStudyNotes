# Python 基础语法

## 01. 编码

默认情况下，Python 3 源码文件以 **UTF-8** 编码，所有字符串都是 unicode 字符串。 当然你也可以为源码文件指定不同的编码：
`# -*- coding: gbk -*-`
上述定义允许在源文件中使用 Windows中的简体中文字符编码，对应适合语言为非unicode的简体中文。

## 02. 标识符

* 第一个字符必须是字母表中字母或下划线 `_` 。
* 标识符的其他的部分由字母、数字和下划线组成。
* 标识符对大小写敏感。

在 Python 3 中，非 ASCII 标识符也是允许的，使用中文字符作为标识符也是合法的。

## 03. Python保留字

保留字也称关键字，在程序中不能把它们用作标识符。Python 的标准库提供 keyword 模块，可以输出当前版本的所有关键字：

```Python
>>> import keyword
>>> keyword.kwlist
['False',  'None',  'True',  'and',  'as',  'assert',  'break',  'class',  'continue',  'def',  'del',  'elif',  'else',  'except',  'finally',  'for',  'from',  'global',  'if',  'import',  'in',  'is',  'lambda',  'nonlocal',  'not',  'or',  'pass',  'raise',  'return',  'try',  'while',  'with',  'yield']
```

## 04. 注释

Python中单行注释以 **`#`** 开头，实例如下：

**实例**

```Python
#!/usr/bin/python3
# 上一行表示在命令行直接执行Python文件时所调用的Python解释器
print("Hello, Python!") # 打印输出字符串
```

执行以上代码，输出结果为：

```Text
Hello, Python!
```

多行注释可以用多行 `#` 号，或者使用多行字符串对象作为注释 `'''` 和 `"""`：

**实例**

```Python
# 第一个注释
# 第二个注释

'''
第三注释
第四注释
'''

"""
第五注释
第六注释
"""
print("Hello, Python!")
```

执行以上代码，输出结果为：

```Text
Hello, Python!
```

## 05. 行与缩进

python最具特色的就是使用缩进来表示代码块，不需要使用大括号 `{} `。
缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数。实例如下：

**实例**

```Python
if True:
    print("True")
else:
    print("False")
```

以下代码最后一行语句缩进数的空格数不一致，会导致运行错误：

```Python
if True:
    print("Answer")
    print("True")
else:
    print("Answer")
  print("False")# 缩进不一致，会导致运行错误
```

以上程序由于缩进不一致，执行后会出现类似以下错误：

```Text
print("False")# 缩进不一致，会导致运行错误
                                   ^
IndentationError: unindent does not match any outer indentation level
```

## 06. 多行语句

Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠`\`来实现多行语句，例如：

```Python
total = item_one + \
        item_two + \
        item_three
```

在`[]`，`{}`，或`()`中的多行语句，不需要使用反斜杠`\`，例如：

```Python
total = ['item_one', 
         'item_two', 
         'item_three', 
         'item_four', 
         'item_five']
```

## 07. 空行

函数之间或类的方法之间用空行分隔，表示一段新的代码的开始。类和函数入口之间也用一行空行分隔，以突出函数入口的开始。

空行与代码缩进不同，空行并不是Python语法的一部分。书写时不插入空行，Python解释器运行也不会出错。但是空行的作用在于分隔两段不同功能或含义的代码，便于日后代码的维护或重构。

**记住：**空行也是程序代码的一部分。


## 08.  同一行显示多条语句(不建议使用此类语法)

Python可以在同一行中使用多条语句，语句之间使用分号(;)分割，以下是一个简单的实例：

**实例**

```Python
import sys; x = 'TechLab'; sys.stdout.write(x + '\n')
```

执行以上代码，输出结果为：

```Text
TechLab
```

## 09. 多个语句构成代码组

缩进相同的一组语句构成一个代码块，我们称之代码组。

像if、while、def和class这样的复合语句，首行以关键字开始，以冒号( : )结束，该行之后的一行或多行代码构成代码组。

我们将首行及后面的代码组称为一个子句(clause)。

如下实例：

```Python
if expression : 
    suite
    suite
    suite
elif expression : 
    suite 
else : 
    suite
```

## 10. input 输入

执行下面的程序在按回车键后就会等待用户输入：

**实例**

```Python
input("\n\n按下 enter 键后退出。")
```

以上代码中 ，"\n\n"在结果输出前会输出两个新的空行（输出中的空行）。

一旦用户按下<kbd>Enter</kbd>键时，程序将退出。


## 11. print 输出

print 默认输出是换行的，如果要实现不换行需要在变量末尾加上 **end=""**：

**实例**

```Python
x="a"
y="b"
# 换行输出
print(x)
print(y)
 
print('---------')
# 不换行输出
print(x, end="")
print(y, end="")
print()
```

以上实例执行结果为：

```Text
a
b
---------
a b
```

## 12. import 与 from...import

在 python 用`import`或者`from...import`来导入相应的模块。

将整个模块(somemodule)导入（相当于导入的是一个文件夹，是个相对路径），格式为：
`import somemodule`
从某个模块中导入某个函数（相当于导入的是一个文件夹中的文件，是个绝对路径）,格式为：
`from somemodule import somefunction`
从某个模块中导入多个函数,格式为： 
`from somemodule import firstfunc, secondfunc, thirdfunc`

将某个模块中的全部函数导入，格式为：`from somemodule import *`

**导入 sys 模块**

```Python
import sys  # 导入 sys 模块
print('================Python import mode==========================')
print('命令行参数为:')
for i in sys.argv:
    print(i)
print('Python 路径为:',sys.path)
```

**导入 sys 模块的 argv,path 成员**

```Python
from sys import argv, path  # 导入 sys 模块中特定的成员

print('================python from import========================')
print('命令行参数为:')
for i in argv:  # 因为已经导入argv成员，所以此处引用时不需要加sys.argv
    print(i)
print('Python 路径为:', path)  # 因为已经导入path成员，所以此处引用时不需要加sys.path
```

## 13. Python脚本的运行方式

1. **交互式：**
在终端启动 Python，以交互式编程模式运行，适合于小段代码的测试
2. **脚本式：**
在终端以 `python [FileName].py` 的形式运行已保存的 Python 脚本文件，适合于较大型项目文件的运行