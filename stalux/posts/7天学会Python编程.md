---
title: 【Python】7天学会编程
tags:
  - 编程开发
  - Python
categories:
  - 编程开发
date: 2025-12-16T11:00:00+08:00
updated: 2026-1-26T12:00:00+08:00
abbrlink: "【Python】7天学会编程"
---



# 【Python】7天学会编程

### 配套视频教程

>

目标：

* 掌握 Python3 环境搭建、PyCharm 基本配置与操作，简单了解辅助 Python 编程的 AI 工具。

* 掌握 Python 基础语法规则和常见基本数据类型。

* 熟悉 Python 中常用的几种基础数据结构。

* 学习更多数据结构，并掌握代码的条件和循环控制。

* 学习 Python 一些进阶语法和函数相关知识。

* 学习 Python 模块的使用，以及输入输出和文件操作相关知识。

* 学习 Python 错误处理机制和面向对象编程相关知识。



### 初识 Python 与环境准备

#### 初识 Python 基本情况

python 是一门高级编程语言，融合了解释性、编译性、互动性特点，同时支持面向对象编程。

它的设计着重强调可读性，与其他编程语言相比，Python 更常使用英文关键字，而非过多依赖标点符号，语法结构独具特色。

作为解释型语言，Python 省去了开发过程中的编译步骤，这点与 PHP、Perl 类似。

其交互式特性允许开发者在 Python 提示符 》》》 后直接运行代码，十分便捷。

在编程范式上，Python 支持面向对象风格，能将代码封装到对象中进行编程。

对于编程初学者来说，Python 是绝佳的选择。它适用范围广泛

#### 环境准备

Python3 最新源码，二进制文档，新闻资讯等可以在 Python 的官网查看到：

Python 官网：<https://www.python.org/>

你可以在以下链接中下载 Python 的文档，你可以下载 HTML、PDF 和 PostScript 等格式的文档。

Python文档下载地址：<https://www.python.org/doc/>



### 第一天：Python3 环境



#### Python3 环境搭建

Python3 可应用于多平台包括 Windows、Linux 和 Mac OS X。

##### Python的安装

以下是各平台python安装包的下载地址



**Source Code** 可用于 Linux 上的安装

以下为不同平台上安装 Python3 的步骤：



##### Unix & Linux 平台安装 Python3

###### 方法一：通过系统包管理器安装（推荐新手）

适用于 Debian/Ubuntu、CentOS/RHEL 等主流发行版，简单稳定。

1. **更新包索引**

   * Debian/Ubuntu 系统：

   ```bash
   sudo apt update
   ```

   * CentOS/RHEL 系统（需先启用 EPEL 源）：

   ```bash
   sudo yum install epel-release
   sudo yum update
   ```

2. **安装 Python3**

   * Debian/Ubuntu 系统：

   ```bash
   sudo apt install python3
   ```

   * CentOS/RHEL 系统：

   ```bash
   sudo yum install python3
   ```

3. **验证安装**输入以下命令查看版本，确认安装成功：

```bash
python3 --version
```



###### 方法二：从源码编译安装（适合需要特定版本）

当系统包管理器中的 Python3 版本不符合需求时使用。



**下载 Python3 源码**从 [Python 官网](https://www.python.org/downloads/source/) 获取对应版本的源码包（以 3.11.6 为例）：

1. 打开 WEB 浏览器访问 <https://www.python.org/downloads/source/>  ，下载对应的包，上传到linux的某个目录下

* **解压并编译**



```bash
tar -xf Python-3.11.6.tgz
cd Python-3.11.6
./configure --enable-optimizations  # 启用优化，提升性能make -j 4  # 多线程编译（4 为 CPU 核心数，可调整）sudo make altinstall  # 避免覆盖系统默认 Python
```

* **验证安装**

```bash
python3.11 --version  # 注意版本号需与安装的一致
```



##### Window 平台安装 Python

1. 打开 WEB 浏览器访问 <https://www.python.org/downloads/windows/>    下载成功后，双击执行安装

* 记得勾选 **Add Python 3.9 to PATH，选择安装路径**

* 按 **Win+R** 键，输入 cmd 调出命令提示符，输入 python



##### MAC 平台安装 Python

MAC 系统都自带有 Python2.7 环境，你可以在链接 <https://www.python.org/downloads/mac-osx/> 上下载最新版安装 Python 3.x，双击安装，配制环境变量就可以了，但建议按下面方法来安装

###### 使用 Homebrew 安装（推荐）

Homebrew 是 macOS 上一款非常流行的包管理器，使用它安装 Python 简单便捷，还能方便管理 Python 的版本和相关依赖。

1. **检查是否安装 Homebrew**：打开 “终端”（可以通过 “聚焦搜索”，输入 “终端” 打开），在终端中输入以下命令：

```bash
brew --version
```

如果显示 Homebrew 的版本信息，说明已经安装；如果提示命令未找到，则需要安装 Homebrew，安装命令如下：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

按照提示完成安装即可。

2\. **安装 Python**：在终端中输入以下命令安装 Python，以安装 Python 3 为例：



```bash
brew install python
```

Homebrew 会自动处理依赖关系并完成安装。

3\. **验证安装**：安装完成后，在终端中输入以下命令检查 Python 3 的版本：



```bash
python3 --version
```

还可以输入以下命令进入 Python 3 的交互式环境：

```bash
python3
```



#### Python3 pycharm-掌握使用 pycharm这款常用编辑器来编写 Python 代码的基本配置和操作

##### pycharm下载

官网的下载地址是:<http://www.jetbrains.com/pycharm/download/#section=windows>

Professional（专业版，收费）：完整的功能，可试用 30 天。

Community（社区版，免费）：阉割版的专业版。

如果是学习选择下载社区版

##### Pycharm安装

###### Windows 系统安装步骤

1. **下载安装包**

   * 打开浏览器，访问 JetBrains 官方网站（<https://www.jetbrains.com/pycharm/download/> ）。

   * 在下载页面中，根据需求选择版本，点击 Windows 系统对应的下载按钮，下载安装包（通常是 `.exe` 格式）。

2. **运行安装程序**

   * 下载完成后，找到下载的安装包，双击运行。

   * 在安装向导界面，点击 “Next” 进入下一步。

   * 选择安装路径，默认路径是 `C:\Program Files\JetBrains\PyCharm Community Edition <版本号>`，也可以点击 “Browse” 自定义安装路径，然后点击 “Next”。

   

   * 在安装选项界面，可以根据需要勾选创建桌面快捷方式（针对不同位数系统）、将 PyCharm 添加到系统 `PATH` 环境变量等选项，建议全部勾选，方便后续使用，接着点击 “Next”。

   * 确认安装信息无误后，点击 “Install” 开始安装。

3. **安装完成配置**

   * 安装完成后，点击 “Finish” 运行 PyCharm。

   * 首次启动时，会弹出选择主题（Theme）的界面，可以选择 Darcula（深色主题）或 IntelliJ（浅色主题）等，选择后点击 “OK”。

   * 接下来会进入配置设置界面，主要做如下配制。




###### Mac 系统安装步骤

1. **下载安装包**

   * 打开浏览器，进入 JetBrains 官方网站的 PyCharm 下载页面（<https://www.jetbrains.com/pycharm/download/> ）。

   * 选择需要的版本（社区版或专业版），点击 Mac 系统对应的下载按钮，下载 `.dmg` 格式的安装包。

2. **安装 PyCharm**

   * 下载完成后，双击 `.dmg` 文件，打开安装包。

   * 将 PyCharm 图标拖到 “Applications” 文件夹（即应用程序文件夹）中，完成安装。

3. **启动并配置**

   * 打开 “Launchpad”（启动台），找到 PyCharm 图标，点击启动。

   * 首次运行时，会弹出是否导入之前配置的提示框，根据实际情况选择，然后点击 “OK”。

   * 接着是选择主题界面，选择喜欢的主题后点击 “OK”。

   * 后续的配置设置与 Windows 系统类似，如选择功能安装、激活（专业版）等步骤，完成后即可使用。



###### Linux 系统安装步骤（以 Ubuntu 为例，其他发行版类似）

1. **下载安装包**

   * 打开浏览器，访问 JetBrains 官方网站的 PyCharm 下载页面（<https://www.jetbrains.com/pycharm/download/> ）。

   * 选择版本后，点击 Linux 系统对应的下载按钮，下载 `.tar.gz` 格式的压缩包。

2. **解压安装包**

   * 打开终端，使用 `cd` 命令进入下载目录，例如下载到了 `Downloads` 目录，可输入 `cd Downloads`。

   * 输入解压命令，以社区版为例，假设下载的压缩包名为 `pycharm-community-<版本号>.tar.gz`，解压命令为：

```bash
tar -xzvf pycharm-community-<版本号>.tar.gz
```

* 解压完成后，会生成一个对应的文件夹。

3. **启动 PyCharm**

   * 进入解压后的文件夹，例如 `cd pycharm-community-<版本号>/bin`。

   * 在 `bin` 目录下，找到 `pycharm.sh` 文件，输入以下命令赋予执行权限：

```bash
chmod +x pycharm.sh
```

* 然后输入 `./pycharm.sh` 启动 PyCharm。

4. **后续配置**

   * 首次启动会弹出与 Windows、Mac 系统类似的配置界面，包括选择主题、导入配置、激活（专业版）等操作，按照提示完成配置后，即可开始使用 PyCharm。



##### pycharm编写 Python 代码的基本配置和操作

在pycharm中输入代码，在编辑区域右键运行

配制参考windowst系统安装步骤中的**安装完成配置。**



#### Python3 AI 编程助手-简单了解有哪些 AI 工具可以辅助 Python 编程

##### 集成 CodeGeeX 插件（以 Lingma 为例，其他类似插件操作流程近似）

CodeGeeX 是一款基于人工智能的代码生成工具，能辅助开发者快速编写代码。

1. **打开插件设置**在 PyCharm 中，点击菜单栏的 “File”，选择 “Settings”（Windows/Linux）或 “PyCharm” -> “Preferences”（Mac），打开设置窗口。

2. **搜索并安装插件**在设置窗口中，找到并点击 “Plugins”（插件）选项。然后在搜索框中输入 “Lingma”，在搜索结果中找到 “Lingma” 插件，点击 “Install” 进行安装。

* **安装完成后配置与使用**

  * 安装完成后，重启 PyCharm 使插件生效。

  * 重启后，在编写代码时，你可以通过快捷键（默认是 `Ctrl + Enter` 或 `Command + Enter` ，可在设置中修改 ）调出 Lingma的代码生成弹窗，输入代码描述，它会根据描述生成相应的代码片段供你选择和使用。



### 第二天：基础语法与数据类型

#### 基本语法

##### 编码规则

默认情况下，Python3 源码文件以 **UTF-8** 编码，所有字符串都是 unicode 字符串。

当然你也可以为源码文件指定不同的编码

```python
# 默认用UTF-8编码，支持中文
姓名 = "张三"print(姓名)  # 输出：张三# 如需指定其他编码（很少用）
# -*- coding: cp-1252 -*-  # 放在文件第一行
```

##### 标识符规则

* 第一个字符必须以字母（a-z, A-Z）或下划线 **\_** 。

* 标识符的其他的部分由字母、数字和下划线组成。

* 标识符对大小写敏感，count 和 Count 是不同的标识符。

* 标识符对长度无硬性限制，但建议保持简洁（一般不超过 20 个字符）。

* 禁止使用保留关键字，如 if、for、class 等不能作为标识符。

合法标识符如下：

```python
# 合法的变量名
age = 10
my_name = "小明"
_age = 20
MAX_NUM = 100
成绩 = 95  # 支持中文#
```

非法的变量名（会报错）

```python
 2name = "错误"  # 不能以数字开头
 my-name = "错误"  # 不能有连字符
 if = 5  # 不能用关键字
```

##### 关键字查看

保留字即关键字，我们不能把它们用作任何标识符名称。Python 的标准库提供了一个 keyword 模块，可以输出当前版本的所有关键字

```python
import keyword
print(keyword.kwlist)  # 打印所有关键字，比如if、for、class等
```

| 类别   | 关键字      | 说明                  |
| ---- | -------- | ------------------- |
| 逻辑值  | true     | 布尔真值                |
|      | false    | 布尔假值                |
|      | None     | 表示空值或无值             |
| 逻辑运算 | and      | 逻辑与运算               |
|      | or       | 逻辑或运算               |
|      | not      | 逻辑非运算               |
| 条件控制 | if       | 条件判断语句              |
|      | elif     | 否则如果（else if 的缩写）   |
|      | else     | 否则分支                |
| 循环控制 | for      | 迭代循环                |
|      | while    | 条件循环                |
|      | break    | 跳出循环                |
|      | continue | 跳过当前循环的剩余部分，进入下一次迭代 |
| 异常处理 | try      | 尝试执行代码块             |
|      | except   | 捕获异常                |
|      | finally  | 无论是否发生异常都会执行的代码块    |
|      | raise    | 抛出异常                |
| 函数定义 | def      | 定义函数                |
|      | return   | 从函数返回值              |
|      | lambda   | 创建匿名函数              |
| 类与对象 | class    | 定义类                 |
|      | del      | 删除对象引用              |
| 模块导入 | import   | 导入模块                |
|      | from     | 从模块导入特定部分           |
|      | as       | 为导入的模块或对象创建别名       |
| 作用域  | global   | 声明全局变量              |
|      | nonlocal | 声明非局部变量（用于嵌套函数）     |
| 异步编程 | async    | 声明异步函数              |
|      | await    | 等待异步操作完成            |
| 其他   | assert   | 断言，用于测试条件是否为真       |
|      | in       | 检查成员关系              |
|      | is       | 检查对象身份（是否是同一个对象）    |
|      | pass     | 空语句，用于占位            |
|      | with     | 上下文管理器，用于资源管理       |
|      | yield    | 从生成器函数返回值           |

> *更多 Python 保留关键字参考：<https://www.runoob.com/python3/python3-keyword.html>。*

##### 注释

Python中单行注释以 **#** 开头，多行注释可以用多个 **#** 号，还有 **'''** 和 **"""**

```python
# 这是单行注释，一行只写一句说明'''
这是多行注释
可以写很多行
'''print("Hello")  # 这也是注释，在代码后面说明
```

##### 缩进规则

python最具特色的就是使用缩进来表示代码块，不需要使用大括号 **{}** 。

缩进的空格数是可变的，但是同一个代码块的语句必须包含相同的缩进空格数

```python
# 正确的缩进（同一代码块缩进一致）
if 5 > 3:print("5比3大")  # 缩进4个空格
    print("条件成立")  # 同样缩进# 错误的缩进（会报错）# 
    if 5 > 3:#     print("正确")#  
         print("错误")  # 缩进不一致
```

缩进不对，执行后会报错如下：





##### 多行语句

Python 通常是一行写完一条语句，但如果语句很长，我们可以使用反斜杠 \ 来实现多行语句

```python
# 用反斜杠换行
total = 10 + 20 + \
        30 + 40print(total)  # 输出：100# 列表/字典里换行不用反斜杠
fruits = ["苹果","香蕉","橘子"]print(fruits)  # 输出：['苹果', '香蕉', '橘子']
```

##### 数字类型

python中数字有四种类型：整数、布尔型、浮点数和复数。

```python
a = 100  # 整数（int）
b = 3.14  # 浮点数（float）
c = True  # 布尔值（True/False）
d = 2 + 3j  # 复数（很少用）print(a + b)  # 输出：103.14（不同类型可运算）
```

##### 字符串操作

ython 中单引号 ' 和双引号 " 使用完全相同。

使用三引号(''' 或 """)可以指定一个多行字符串。

转义符 \。

```python
# 字符串定义
s1 = "hello"
s2 = 'world'
s3 = """这是
多行
字符串"""# 拼接和重复
print(s1 + " " + s2)  # 输出：hello world
print(s1 * 2)  # 输出：hellohello# 索引（取单个字符）
print(s1[0])  # 输出：h（第1个字符）print(s1[-1])  # 输出：o（最后1个字符）# 切片（取一段字符）
print(s1[1:4])  # 输出：ell（从第2个到第4个）# 原始字符串（不转义）
print(r"c:\test")  # 输出：c:\test（\不转义）
```

##### 用户输入



```python
name = input("请输入你的名字：")
print("你好，" + name)  # 输入什么就打印什么# 示例：输入后按回车继续
input("按回车结束...")
```

##### 同一行多条语句



```python
a = 1; b = 2; c = a + b
print(c)  # 输出：3（一行写3条语句）
```

##### print 输出

**print** 默认输出是换行的，如果要实现不换行需要在变量末尾加上 end=""

```python
# 默认换行
print("第一行")
print("第二行")# 不换行（用end指定分隔符）
print("苹果", end="、")
print("香蕉", end="、")
print("橘子")  # 输出：苹果、香蕉、橘子
```



> **更多内容参考：**[Python2 与 Python3 print 不换行](https://www.runoob.com/w3cnote/python-print-without-newline.html)

##### 模块导入

###### import 与 from...import

在 python 用 import 或者 from...import 来导入相应的模块。

将整个模块(somemodule)导入，格式为： import somemodule

从某个模块中导入某个函数,格式为： from somemodule import somefunction

从某个模块中导入多个函数,格式为： from somemodule import firstfunc, secondfunc, thirdfunc

将某个模块中的全部函数导入，格式为： from somemodule import \*

```python
# 导入整个模块import math
print(math.sqrt(16))  # 输出：4.0（计算平方根）# 导入模块中的部分功能
from math import sqrt
print(sqrt(25))  # 输出：5.0（直接用sqrt，不用加math.）
```



#### &#x20;基本数据类型

Python 中的变量无需声明，使用前必须赋值，赋值后变量才会被创建。变量本身无类型，所谓 “类型” 指的是变量所指向内存中对象的类型，等号（`=`）是变量赋值运算符，左侧为变量名，右侧为变量存储的值。

##### 变量赋值与类型

1. 基础赋值实例



```python
#!/usr/bin/python3
student_id = 2025001    # 整型变量
score = 92.5            # 浮点型变量
student_name = "Lily"   # 字符串print(student_id)  # 输出：2025001print(score)       # 输出：92.5print(student_name)# 输出：Lily
```

* 多变量赋值

- 多变量赋同一值：创建一个对象，从后向前赋值，如 `x = y = z = 0`，三个变量均为 0。

- 多变量赋不同值：按顺序为变量分配对应对象，如 `fruit, price, in_stock = "apple", 5.8, True`，fruit="apple"、price=5.8、in\_stock=True。

* 查看变量类型

使用 `type()` 函数可查询变量指向对象的类型，示例如下：



```python
# 变量定义
age = 22               # 整数
weight = 52.3          # 浮点数
hobby = "reading"      # 字符串
is_student = True      # 布尔值# 查看数据类型
print(type(age))        # 输出：<class 'int'>
print(type(weight))     # 输出：<class 'float'>
print(type(hobby))      # 输出：<class 'str'>
print(type(is_student)) # 输出：<class 'bool'>
```

##### Python3 标准数据类型

Python3 有 6 种标准数据类型，按 “是否可变” 可分为两类：

* **不可变数据**（3 种）：Number（数字）、String（字符串）、Tuple（元组）

* **可变数据**（3 种）：List（列表）、Dictionary（字典）、Set（集合）此外还有高级类型如 `bytes`（字节数组）。

###### Number（数字）

支持 `int`（整数）、`float`（浮点数）、`bool`（布尔值）、`complex`（复数）四种类型，Python3 中仅有一种整数类型 `int`，无 Python2 中的 `Long`。

（1）类型示例与判断



```python
# 赋值不同数字类型
num1, num2, flag, comp = 50, 3.14, False, 2+5j
print(type(num1), type(num2), type(flag), type(comp))  # 输出：<class 'int'> <class 'float'> <class 'bool'> <class 'complex'># 使用 isinstance 判断类型
num = 200
print(isinstance(num, int))  # 输出：True
```

（2）`type()` 与 `isinstance()` 的区别

* `type()`：不认为子类是父类类型，如 `type(Dog()) == Animal` 会返回 `False`（Dog 是 Animal 的子类）。

* `isinstance()`：认为子类是父类类型，如 `isinstance(Dog(), Animal)` 会返回 `True`（Dog 是 Animal 的子类）。

（3）布尔类型特殊说明

* `bool` 是 `int` 的子类，`True == 1`、`False == 0` 均返回 `True`，但建议用 `==` 比较值，而非 `is`（`is` 比较对象身份，可能触发 `SyntaxWarning`）。

* 示例：`True + 2 = 3`、`False + 3 = 3`。

（4）删除变量与数值运算

* 删除变量：使用 `del` 语句，如 `del num`（删除单个变量）、`del num1, num2`（删除多个变量）。

&#x20;数值运算示例：



```python
>>> 8 + 3  # 加法：
11
>>> 6.5 - 2 # 减法：
4.5
>>> 4 * 9  # 乘法：
36
>>> 7 / 2  # 除法（浮点数）：
3.5
>>> 7 // 2 # 除法（整数）：
3
>>> 19 % 4 # 取余：
3
>>> 3 ** 4 # 乘方：
81
```

数字类型实例表

| int（整数） | float（浮点数） | complex（复数） |
| ------- | ---------- | ----------- |
| 30      | 2.5        | 1.2j        |
| -150    | -6.8       | 8.j         |
| 0x4A    | 1500       | 4.2e-2j     |

###### String（字符串）

用单引号（`'`）或双引号（`"`）包裹，反斜杠（`\`）转义特殊字符，支持索引、截取、拼接等操作。

（1）字符串截取语法

`变量[头下标:尾下标]`，索引从左到右以 0 开始，从右到左以 -1 开始，截取结果不包含尾下标对应的字符。

（2）常用操作实例



```python
#!/usr/bin/python3
msg = 'Python'  # 定义字符串print(msg)           # 输出完整字符串：Python
print(msg[0:-1])     # 输出第 1 到倒数第 2 个字符：Pytho
print(msg[1])        # 输出第 2 个字符：y
print(msg[3:6])      # 输出第 4 到第 6 个字符：hon
print(msg[4:])       # 输出第 5 个字符到末尾：on
print(msg * 2)       # 复制字符串两次：PythonPython
print(msg + "Learn") # 拼接字符串：PythonLearn
```

（3）特殊字符处理

* 原始字符串：在字符串前加 `r`，使反斜杠不转义，如 `print(r'Py\thon')` 输出 `Py\thon`。

* 跨多行字符串：使用 `"""..."""` 或 `'''...'''`，如：



```python
print("""I love
Python
programming""")
```

> #### 注意事项

* Python 无单独字符类型，单个字符是长度为 1 的字符串。

* 字符串不可修改，如 `msg[0] = 'p'` 会报错。

###### bool（布尔类型）

仅含 `True`（真）和 `False`（假）两个值，用于控制程序流程（如条件判断），可与逻辑运算符结合使用。

（1）核心特点

* `bool` 是 `int` 子类，`True` 等价于 1，`False` 等价于 0。

* 用 `bool()` 函数转换其他类型：`None`、0（含 0.0、0j）、空序列（`''`、`()`、`[]`）、空映射（`{}`）转换后为 `False`，其余为 `True`。

（2）使用实例



```python
# 布尔值与类型
is_open = True
is_closed = Falseprint(type(is_open))  # 输出：<class 'bool'># 转换与运算
print(bool(0.0))       # 输出：False
print(bool('Hello'))   # 输出：True
print(True or False)   # 逻辑或：True
print(10 < 5)          # 比较运算：False# 条件判断应用
count = 5if count > 0:  # count 大于 0，视为 True
print("数量为正数")
```

###### List（列表）

写在方括号（`[]`）中，元素用逗号分隔，支持不同类型元素（含嵌套列表），可修改、索引、截取，是 Python 中最常用的数据类型之一。

（1）基础操作实例



```python
#!/usr/bin/python3
shopping_list = ['milk', 3, 12.8, 'bread', 2]
snack_list = ['chocolate', 5]print(shopping_list)            # 输出完整列表：['milk', 3, 12.8, 'bread', 2]print(shopping_list[0])         # 输出第 1 个元素：milkprint(shopping_list[2:4])       # 输出第 3 到第 4 个元素：[12.8, 'bread']print(shopping_list[3:])        # 输出第 4 个元素到末尾：['bread', 2]print(snack_list * 2)           # 复制列表两次：['chocolate', 5, 'chocolate', 5]print(shopping_list + snack_list) # 拼接列表：['milk', 3, 12.8, 'bread', 2, 'chocolate', 5]
```

（2）修改列表元素

列表元素可直接修改，示例如下：



```python
nums = [2, 4, 6, 8, 10]
nums[1] = 5  # 修改第 2 个元素
nums[3:5] = [9, 11]  # 修改第 4 到第 5 个元素
print(nums)  # 输出：[2, 5, 6, 9, 11]

nums[2:4] = []  # 删除第 3 到第 4 个元素
print(nums)      # 输出：[2, 5, 11]
```

（3）列表截取进阶

支持第三个参数（步长），示例如下：



```python
# 步长为 2，截取索引 0 到 5 的元素
num_list = [10,20,30,40,50,60]
print(num_list[0:5:2])  # 输出：[10,30,50]# 步长为 -1，逆向读取（翻转列表）
def reverseSentence(sentence):
    words = sentence.split(" ")
    words = words[-1::-1]  # 逆向读取
    new_sentence = ' '.join(words)
    return new_sentence

sentence = 'She loves coding'
print(reverseSentence(sentence))  # 输出：coding loves She
```

###### Tuple（元组）

与列表类似，写在小括号（`()`）中，元素不可修改，支持索引、截取、拼接，可视为 “不可变的列表”。

（1）基础操作实例



```python
#!/usr/bin/python3
book_info = ('Python Basics', 39.9, 2024, 'John')
author_info = ('John', 45)print(book_info)             # 输出完整元组：('Python Basics', 39.9, 2024, 'John')print(book_info[1])          # 输出第 2 个元素：39.9print(book_info[2:4])        # 输出第 3 到第 4 个元素：(2024, 'John')print(author_info * 2)       # 复制元组两次：('John', 45, 'John', 45)print(book_info + author_info) # 拼接元组：('Python Basics', 39.9, 2024, 'John', 'John', 45)
```

（2）特殊注意事项

* 元组元素不可修改，如 `book_info[0] = 'Python 101'` 会报错（`TypeError`）。

* 元组可包含可变元素（如列表），如 `tup = (5, [1,2])`，可修改列表元素 `tup[1][1] = 3`。

* 空元组定义：`empty_tup = ()`；单个元素元组需加逗号：`single_tup = (3.14,)`（否则会被视为普通值）。

###### Set（集合）

无序、可变的唯一元素集合，用大括号（`{}`）表示，或通过 `set()` 函数创建，支持交集、并集、差集等运算。

（1）基础操作实例

```python
#!/usr/bin/python3
fruits = {'apple', 'banana', 'orange', 'apple', 'grape'}print(fruits)   # 输出集合（去重）：{'apple', 'banana', 'orange', 'grape'}# 成员测试if 'banana' in fruits:print('香蕉在集合中')else:print('香蕉不在集合中')# 集合运算
set1 = set('abcdef')
set2 = set('cdefgh')print(set1 - set2)     # 差集：{'a', 'b'}print(set1 | set2)     # 并集：{'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h'}print(set1 & set2)     # 交集：{'c', 'd', 'e', 'f'}print(set1 ^ set2)     # 不同时存在的元素：{'a', 'b', 'g', 'h'}
```

> #### 注意事项

* 创建空集合需用 `set()`，而非 `{}`（`{}` 用于创建空字典）。

* 集合元素唯一，重复元素会被自动去除。

###### Dictionary（字典）

无序的 “键 - 值”（`key:value`）映射类型，用大括号（`{}`）表示，`key` 需为不可变类型且唯一，通过 `key` 存取元素（而非索引）。

（1）基础操作实例



```python
#!/usr/bin/python3
car = {}
car['brand'] = "Toyota"
car['year'] = 2023
phone = {'brand': 'Huawei', 'model': 'Mate 60', 'price': 5999}
print(car['brand'])       # 输出 key='brand' 的值：Toyota
print(car['year'])        # 输出 key='year' 的值：2023
print(phone)              # 输出完整字典：{'brand': 'Huawei', 'model': 'Mate 60', 'price': 5999}print(phone.keys())       # 输出所有 key：dict_keys(['brand', 'model', 'price'])print(phone.values())     # 输出所有 value：dict_values(['Huawei', 'Mate 60', 5999])
```

（2）字典创建方式

除直接赋值外，可通过 `dict()` 函数或字典推导式创建：



```python
# 用键值对序列创建
print(dict([('name', 'Mike'), ('age', 25), ('city', 'Beijing')]))  # 输出：{'name': 'Mike', 'age': 25, 'city': 'Beijing'}
# 用字典推导式创建
print({k: k*2 for k in (1, 2, 3)})  # 输出：{1: 2, 2: 4, 3: 6}
# 用关键字参数创建
print(dict(brand='Apple', product='iPhone', color='black')) 
# 输出：{'brand': 'Apple', 'product': 'iPhone', 'color': 'black'}
```

###### bytes 类型

不可变的二进制序列，元素为 0-255 的整数，用于处理二进制数据（如图片、音频），通过 `b` 前缀或 `bytes()` 函数创建。

（1）创建与操作实例



```python
# 用 b 前缀创建
data = b"example"print(data)  # 输出：b'example'# 用 bytes() 函数创建（指定编码）
binary_data = bytes("example", encoding="utf-8")
print(binary_data)  # 输出：b'example'# 切片与拼接
print(data[2:5])          # 切片：b'amp'
print(data + b"test")     # 拼接：b'exampletest'# 元素比较（需用整数）
if data[0] == ord("e"):  # ord() 转换字符为整数
print("第一个元素是 'e'")
```

#### Python 数据类型转换

通过内置函数可实现不同类型间的转换，函数返回新对象，原对象不变，常用转换函数如下表：

| 函数                     | 描述                            |
| ---------------------- | ----------------------------- |
| int(x \[,base])        | 将 x 转换为整数，base 可选（表示进制，默认 10） |
| float(x)               | 将 x 转换为浮点数                    |
| complex(real \[,imag]) | 创建复数，real 为实部，imag 为虚部（默认 0）  |
| str(x)                 | 将对象 x 转换为字符串                  |
| repr(x)                | 将对象 x 转换为表达式字符串               |
| eval(str)              | 计算字符串中的 Python 表达式，返回结果对象     |
| tuple(s)               | 将序列 s 转换为元组                   |
| list(s)                | 将序列 s 转换为列表                   |
| set(s)                 | 将序列 s 转换为可变集合                 |
| dict(d)                | 创建字典，d 需为 (key, value) 元组序列   |
| frozenset(s)           | 将序列 s 转换为不可变集合                |
| chr(x)                 | 将整数 x 转换为对应字符（x 为 Unicode 码）  |
| ord(x)                 | 将字符 x 转换为对应整数（Unicode 码）      |
| hex(x)                 | 将整数 x 转换为十六进制字符串              |
| oct(x)                 | 将整数 x 转换为八进制字符串               |

#### &#x20;数据类型转换

##### Python 数据类型转换详解

Python 中数据类型转换主要分两类：**隐式转换**（自动完成）和**显式转换**（手动用函数实现），以下用简单实例说明核心逻辑。

##### 隐式类型转换（自动转换）

隐式转换无需手动操作，Python 会根据运算需求，自动将 “范围小 / 精度低” 的类型转为 “范围大 / 精度高” 的类型，避免数据丢失。

###### 整数与浮点数运算（自动转浮点）

整数和浮点数一起运算时，整数会自动变成浮点数，结果也为浮点数：

```python
num1 = 3  # 整数（int）
num2 = 1.5  # 浮点数（float）
result = num1 + num2  # 自动转换：3 → 3.0，再计算
print(result)  # 输出：4.5
print(type(result))  # 输出：<class 'float'>
```

###### 无法自动转换的场景

若两种类型无 “精度 / 范围” 关联（如整数和字符串），Python 无法自动转换，强行运算会报错：



```python
num = 5
text = "10"
print(num + text)  # 报错：TypeError（int 和 str 不能直接相加）
```

##### 显式类型转换（手动转换）

当隐式转换无法满足需求时，需用 `int()`、`float()`、`str()` 等内置函数，手动将数据转为目标类型。

###### 常用基础转换（3 种核心场景）

| 函数       | 功能         | 简单实例                  | 输出结果      |
| -------- | ---------- | --------------------- | --------- |
| int(x)   | 转为整数（舍去小数） | int(2.8)、int("6")     | 2、6       |
| float(x) | 转为浮点数      | float(4)、float("3.5") | 4.0、3.5   |
| str(x)   | 转为字符串      | str(7)、str(9.2)       | "7"、"9.2" |

###### 解决 “整数 + 字符串” 运算问题

用 `int()` 将字符串（需是数字内容）转为整数，再进行运算：



```python
num = 8
text = "12"  # 字符串（数字格式）

text = int(text)  # 手动转换："12" → 12（整数）
total = num + text

print(total)  # 输出：20print(type(total))  # 输出：<class 'int'>
```

##### 其他常用转换函数（按需使用）

除基础类型外，还有针对容器、字符的转换函数，满足更多场景需求：

| 函数        | 功能             | 实例             | 结果      |
| --------- | -------------- | -------------- | ------- |
| tuple(s)  | 列表转元组          | tuple(\[1, 3]) | (1, 3)  |
| list(s)   | 元组转列表          | list((2, 4))   | \[2, 4] |
| chr(x)    | 整数转字符（ASCII 码） | chr(122)       | "z"     |
| ord(x)    | 字符转整数（ASCII 码） | ord("A")       | 65      |
| eval(str) | 执行字符串表达式       | eval("1+2\*3") | 7       |

#### &#x20;运算符

##### 什么是运算符？

运算符是 Python 中用于对 “操作数” 进行计算或判断的特殊符号。比如 `3 * 4 = 12` 中，`3` 和 `4` 是操作数，`*` 就是运算符。Python 支持多种运算符，以下按类型详细说明，实例均为简化版。

算术运算符

用于执行加减乘除等数学运算，假设 `a=8`，`b=3`：

| 运算符  | 描述       | 实例       | 结果       |
| ---- | -------- | -------- | -------- |
| +    | 加        | a + b    | 11       |
| -    | 减        | a - b    | 5        |
| \*   | 乘        | a \* b   | 24       |
| /    | 除（得浮点数）  | a / b    | 2.666... |
| %    | 取模（得余数）  | a % b    | 2        |
| \*\* | 幂（几次方）   | a \*\* b | 512      |
| //   | 取整除（去小数） | a // b   | 2        |

**实例**：



```python
a = 8
b = 3print(a + b)  # 输出 11
print(a % b)  # 输出 2（8除以3余2）
print(a ** 2) # 输出 64（8的2次方）
```

比较运算符

用于比较两个值的关系，结果为 `True`（真）或 `False`（假），假设 `a=5`，`b=7`：

| 运算符 | 描述   | 实例     | 结果    |
| --- | ---- | ------ | ----- |
| ==  | 等于   | a == b | false |
| !=  | 不等于  | a != b | true  |
| >   | 大于   | a > b  | false |
| <   | 小于   | a < b  | true  |
| >=  | 大于等于 | a >= 5 | true  |
| <=  | 小于等于 | b <= 6 | false |

**实例**：



```python
a = 5
b = 7print(a < b)   # 输出 True（5小于7）
print(b == 7)  # 输出 True（7等于7）
print(a >= 6)  # 输出 False（5不大于等于6）
```

赋值运算符

用于给变量赋值，可结合算术运算简化写法，假设初始 `c=4`：

| 运算符 | 描述     | 实例      | 等效写法       |
| --- | ------ | ------- | ---------- |
| =   | 基础赋值   | c = 4   | -          |
| +=  | 加后赋值   | c += 2  | c = c + 2  |
| -=  | 减后赋值   | c -= 1  | c = c - 1  |
| \*= | 乘后赋值   | c \*= 3 | c = c \* 3 |
| //= | 取整除后赋值 | c //= 2 | c = c // 2 |

**实例**：



```python
c = 4
c += 2  # 等效 c = 4 + 2
print(c)  # 输出 6

c *= 3  # 等效 c = 6 * 3
print(c)  # 输出 18
```

> **特殊：海象运算符 `:=`**&#x50;ython 3.8+ 新增，可在表达式中同时赋值和返回结果：



```python
# 直接在判断中赋值并使用
if (num := len([1,2,3])) > 2:print(f"列表长度是 {num}")  # 输出 列表长度是 3
```

位运算符

按二进制位进行计算，需先将数字转为二进制，假设 `a=6`（二进制 `0110`），`b=3`（二进制 `0011`）：

| 运算符 | 描述            | 实例           | 二进制计算              | 结果  |        |               |   |
| --- | ------------- | ------------ | ------------------ | --- | ------ | ------------- | - |
| &   | 按位与（同 1 得 1）  | a & b        | 0110 & 0011 = 0010 | 2   |        |               |   |
| \`  | \`            | 按位或（有 1 得 1） | \`a                | b\` | \`0110 | 0011 = 0111\` | 7 |
| <<  | 左移（高位丢，低位补 0） | a << 1       | 0110 << 1 = 1100   | 12  |        |               |   |
| >>  | 右移（低位丢，高位补 0） | a >> 1       | 0110 >> 1 = 0011   | 3   |        |               |   |

**实例**：



```python
a = 6  # 0110
b = 3  # 0011
print(a & b)  # 输出 2
print(a << 1) # 输出 12
```

逻辑运算符

用于连接布尔值（`True`/`False`），返回新的布尔值，假设 `x=True`，`y=False`：

| 运算符 | 描述        | 实例      | 结果    |
| --- | --------- | ------- | ----- |
| and | 逻辑与（都真才真） | x and y | false |
| or  | 逻辑或（有真就真） | x or y  | true  |
| not | 逻辑非（取反）   | not y   | true  |

**实例**：



```python
x = True
y = Falseprint(x and y)  # 输出 False
print(not x)    # 输出 False
print(x or y)   # 输出 True
```

成员运算符

判断值是否在序列（列表、字符串等）中，返回 `True`/`False`：

| 运算符    | 描述    | 实例               | 结果    |
| ------ | ----- | ---------------- | ----- |
| in     | 在序列中  | 3 in \[1,2,3]    | true  |
| not in | 不在序列中 | 'a' not in 'abc' | false |

**实例**：



```python
my_list = [10, 20, 30]print(20 in my_list)      # 输出 True
print(40 not in my_list)  # 输出 True

my_str = "hello"print('h' in my_str)      # 输出 True
```

身份运算符

判断两个变量是否引用同一个对象（内存地址相同），返回 `True`/`False`：

| 运算符    | 描述     | 实例         | 结果 |
| ------ | ------ | ---------- | -- |
| is     | 引用同一对象 | a is b     | -  |
| is not | 引用不同对象 | a is not b | -  |

**实例**：



```python
a = [1,2]
b = a  # b 和 a 引用同一个列表
print(a is b)  # 输出 True

c = [1,2]  # c 是新列表（内存地址不同）
print(a is c)  # 输出 False
print(a == c)  # 输出 True（值相等，但不是同一对象）
```

运算符优先级

不同运算符的计算顺序不同，优先级高的先算；优先级相同则从左到右（除幂运算从右到左）。**核心优先级（从高到低）**：

1. 括号 `()`（可强制改变顺序）

2. 幂运算 `**`

3. 算术运算（`*`/`/` 高于 `+`/`-`）

4. 比较运算（`==`/`>`/`<` 等）

5. 逻辑运算（`not` 高于 `and`，`and` 高于 `or`）

**实例**：



```python
# 无括号：先算 * 再算 +
print(2 + 3 * 4)  # 输出 14（3*4=12，2+12=14）# 有括号：先算括号内
print((2 + 3) * 4)  # 输出 20（2+3=5，5*4=20）# 逻辑运算优先级
print(True or False and False)  # 输出 True（先算 and，再算 or）
```



### 第三天：常用数据结构（一）

#### python3 数字（Number）

数字数据类型用于存储数值，其特性是**不可变**（修改值时会重新分配内存）。

##### 数字类型分类

Python 支持三种基本数字类型：

1. **整型（int）**

   * 正 / 负整数，无小数点，大小无限制（Python 3 无 long 类型）。

   * 支持十进制、十六进制（前缀 `0x`）、八进制（前缀 `0o`）。

   * 示例：`10`、`-20`、`0x1A`（十进制 26）、`0o75`（十进制 61）。

2. **浮点型（float）**

   * 含整数和小数部分，支持科学计数法（如 `2.5e3` 即 2500）。

   * 示例：`3.14`、`-0.5`、`1e-2`（0.01）。

3. **复数（complex）**

   * 由实部和虚部组成，格式为 `a + bj`（`j` 为虚数单位）。

   * 示例：`3+4j`、`complex(2, 5)`（等价于 `2+5j`）。

##### 变量操作

* **创建**：直接赋值即可，如 `num = 100`。

* **删除引用**：用 `del` 语句，如 `del num` 或 `del a, b`（删除多个）。

##### 类型转换

通过类型函数可相互转换：

* `int(x)`：转为整型（如 `int(3.8)` → `3`）。

* `float(x)`：转为浮点型（如 `float(5)` → `5.0`）。

* `complex(x)`：转为复数（如 `complex(4)` → `4+0j`）。

* `complex(x, y)`：用 x（实部）和 y（虚部）创建复数（如 `complex(2, 3)` → `2+3j`）。

##### 数字运算

支持常见数学运算，示例：

```python
# 基础运算
print(5 + 3)   # 加法 → 8
print(10 - 4)  # 减法 → 6
print(3 * 7)   # 乘法 → 21
print(15 / 4)  # 除法（得浮点数）→ 3.75
print(15 // 4) # 取整除（去小数）→ 3
print(15 % 4)  # 取模（余数）→ 3
print(2 **3)  # 幂运算（2的3次方）→ 8# 混合运算（自动转为浮点型）
print(3 + 2.5)  # → 5.5
```

##### 数学函数（需导入 `math` 模块）

常用函数示例：

* `abs(x)`：绝对值（`abs(-5)` → `5`）。

* `math.ceil(x)`：向上取整（`math.ceil(2.1)` → `3`）。

* `math.floor(x)`：向下取整（`math.floor(2.9)` → `2`）。

* `max(x1, x2...)`：最大值（`max(1,3,5)` → `5`）。

* `min(x1, x2...)`：最小值（`min(1,3,5)` → `1`）。

* `round(x, n)`：四舍五入（`round(3.1415, 2)` → `3.14`）。

* `math.sqrt(x)`：平方根（`math.sqrt(16)` → `4.0`）。

##### 随机数函数（需导入 `random` 模块）

常用函数示例：

* `random.choice(seq)`：从序列随机选元素（`random.choice([1,2,3])` → 随机 1/2/3）。

* `random.random()`：生成 \[0,1) 随机浮点数。

* `random.shuffle(lst)`：随机打乱列表（如 `lst = [1,2,3]` → 打乱后顺序随机）。

##### 三角函数（需导入 `math` 模块）

* 如 `math.sin(x)`（正弦）、`math.cos(x)`（余弦），参数为弧度。

* 角度与弧度转换：`math.radians(90)`（90 度转弧度）、`math.degrees(math.pi/2)`（弧度转 90 度）。

##### 数学常量

* `math.pi`：圆周率（≈3.14159...）。

* `math.e`：自然常数（≈2.71828...）。



#### Python3 字符串

字符串是 Python 中最常用的数据类型，用单引号（`'`）或双引号（`"`）创建，例如：



```python
str1 = 'Hello Python'
str2 = "编程学习"
```

##### 访问字符串

通过索引（`[]`）截取子字符串，索引从 `0` 开始（正向）或 `-1` 开始（反向），语法：`变量[头下标:尾下标]`（左闭右开，不包含尾下标字符）。

**实例**：



```python
text = "abcdef"
print(text[0])      # 取第1个字符 → 'a'
print(text[2:5])    # 取索引2到4的字符 → 'cde'
print(text[-3:])    # 取最后3个字符 → 'def'
```

##### 字符串更新

通过截取拼接实现 “更新”（字符串不可变，实际是创建新字符串）。

**实例**：



```python
old_str = "I like cats"
new_str = old_str[:7] + "dogs"  # 替换后半部分
print(new_str)  # 输出：I like dogs
```

##### 转义字符

用反斜杠（`\`）表示特殊字符，常见转义字符：

| 转义字符 | 描述         | 实例                        | 输出结果         |
| ---- | ---------- | ------------------------- | ------------ |
| \n   | 换行         | print("第一行\n第二行")         | 第一行第二行       |
| \t   | 横向制表符（Tab） | print("姓名\t年龄")           | 姓名 年龄        |
| \\'  | 单引号        | print('It\\'s good')      | It's good    |
| \\"  | 双引号        | print("He said \\"Hi\\"") | He said "Hi" |
| \\\\ | 反斜杠        | print("路径：C:\\\data")     | 路径：C:\data   |

**实例（进度条）**：



```python
import time
for i in range(101):# \r 使光标回到行首，实现覆盖输出
print(f"\r进度：{i}%", end='')
    time.sleep(0.1)  # 延迟0.1秒
```

##### 字符串运算符

假设 `a = "hi"`，`b = "python"`：

| 运算符    | 描述         | 实例           | 结果         |
| ------ | ---------- | ------------ | ---------- |
| +      | 连接字符串      | a + b        | "hipython" |
| \*     | 重复输出       | a \* 2       | "hihi"     |
| in     | 判断是否包含     | "h" in a     | true       |
| not in | 判断是否不包含    | "x" not in b | true       |
| r/R    | 原始字符串（不转义） | print(r"\n") | \n         |

**实例**：



```python
a = "hi"
b = "python"print(a + " " + b)  # 输出：hi python
print(b * 2)        # 输出：pythonpython
print("y" in b)     # 输出：True
```

##### 字符串格式化

多种方式格式化字符串，常用以下两种：

1. **% 格式化**用 `%` 占位符替换变量，例如：

```python
name = "小明"
age = 12
print("姓名：%s，年龄：%d岁" % (name, age))  # 输出：姓名：小明，年龄：12岁
```

1. 常用占位符：`%s`（字符串）、`%d`（整数）、`%f`（浮点数）。

2. **f-string（Python 3.6+）**&#x524D;缀 `f` + 大括号 `{}` 嵌入变量 / 表达式，例如：



```python
score = 95
print(f"得分：{score}，等级：{ '优秀' if score >= 90 else '良好' }")# 输出：得分：95，等级：优秀
```

##### 三引号

用 `'''` 或 `"""` 定义多行字符串，保留换行和缩进。

**实例**：

python

运行

```python
multi_line = """这是第一行
这是第二行
    这是缩进的第三行"""
    print(multi_line)# 输出：# 这是第一行# 这是第二行#     这是缩进的第三行
```

##### 常用内建函数

字符串自带多种方法，简化操作：

| 方法                    | 描述     | 实例                       | 结果             |
| --------------------- | ------ | ------------------------ | -------------- |
| len(str)              | 计算长度   | len("hello")             | 5              |
| str.upper()           | 转大写    | "abc".upper()            | "ABC"          |
| str.lower()           | 转小写    | "ABC".lower()            | "abc"          |
| str.split(sep)        | 按分隔符拆分 | "a,b,c".split(",")       | \["a","b","c"] |
| str.join(seq)         | 拼接序列元素 | "-".join(\["a","b"])     | "a-b"          |
| str.replace(old, new) | 替换子串   | "aaa".replace("a","b",2) | "bba"          |
| str.strip()           | 去除首尾空格 | " test ".strip()         | "test"         |

**实例**：



```python
s = "  Hello World  "print(s.strip())          # 输出：Hello World
print(s.replace("World", "Python"))  # 输出：  Hello Python  
print(s.split())          # 输出：["Hello", "World"]（默认按空格拆分）
```

#### Python3 列表

序列是 Python 基本数据结构，每个元素有索引（从 `0` 开始）。最常用的序列类型是**列表**（可变）和元组（不可变）。

##### 列表的创建

列表用方括号 `[]` 包裹，元素用逗号分隔，数据类型可不同：



```python
fruits = ["苹果", "香蕉", "橙子"]  # 字符串列表
mixed = [10, "hello", True, 3.14]  # 混合类型列表
empty = []  # 空列表
```

##### 访问列表元素

通过索引访问，支持正向（`0` 开始）和反向（`-1` 开始，代表最后一个元素）：

**实例**：



```python
colors = ["红", "绿", "蓝", "黄"]
print(colors[0])   # 正向索引 → "红"
print(colors[-2])  # 反向索引 → "蓝"
print(colors[1:3]) # 切片（左闭右开）→ ["绿", "蓝"]
print(colors[:2])  # 从开头到索引1 → ["红", "绿"]
print(colors[2:])  # 从索引2到结尾 → ["蓝", "黄"]
```

##### 更新列表

列表是可变的，可直接修改元素或添加新元素：

**实例**：



```python
numbers = [1, 2, 3]# 修改元素
numbers[1] = 20
print(numbers)  # 输出：[1, 20, 3]# 添加元素（append() 方法）
numbers.append(4)
print(numbers)  # 输出：[1, 20, 3, 4]# 插入元素（insert() 方法，指定位置）
numbers.insert(0, 0)  # 在索引0插入0
print(numbers)  # 输出：[0, 1, 20, 3, 4]
```

##### 删除列表元素

用 `del` 语句或列表方法删除元素：

**实例**：



```python
animals = ["猫", "狗", "兔", "鸟"]# del 语句删除指定索引元素
del animals[2]
print(animals)  # 输出：["猫", "狗", "鸟"]# remove() 方法删除第一个匹配值
animals.remove("狗")
print(animals)  # 输出：["猫", "鸟"]# pop() 方法删除并返回指定索引元素（默认最后一个）
last = animals.pop()
print(last)     # 输出："鸟"
print(animals)  # 输出：["猫"]
```

##### 列表运算符

支持 `+`（组合）、`*`（重复）、`in`（判断成员）等：

**实例**：



```python
a = [1, 2]
b = [3, 4]
print(a + b)        # 组合 → [1, 2, 3, 4]
print(a * 2)        # 重复 → [1, 2, 1, 2]
print(2 in a)       # 判断成员 → True
print(5 not in b)   # 判断非成员 → True
```

##### 嵌套列表

列表中可包含其他列表（嵌套）：

**实例**：



```python
# 嵌套列表（二维列表）
matrix = [[1, 2, 3],[4, 5, 6],[7, 8, 9]]
print(matrix[1])      # 访问第二行 → [4, 5, 6]
print(matrix[0][2])   # 访问第一行第三列 → 3
```

##### 常用列表函数与方法

| 函数 / 方法          | 描述          | 实例                         | 结果         |
| ---------------- | ----------- | -------------------------- | ---------- |
| len(list)        | 计算长度        | len(\[1,2,3])              | 3          |
| max(list)        | 最大值（元素需可比较） | max(\[5, 2, 8])            | 8          |
| min(list)        | 最小值         | min(\[5, 2, 8])            | 2          |
| list.append(obj) | 末尾添加元素      | a = \[1]; a.append(2)      | \[1, 2]    |
| list.extend(seq) | 末尾追加另一个序列   | a = \[1]; a.extend(\[2,3]) | \[1, 2, 3] |
| list.sort()      | 原地排序（默认升序）  | a = \[3,1,2]; a.sort()     | \[1, 2, 3] |
| list.reverse()   | 原地反转元素      | a = \[1,2,3]; a.reverse()  | \[3, 2, 1] |
| list.count(obj)  | 统计元素出现次数    | \[1,2,2,3].count(2)        | 2          |
| list.copy()      | 复制列表（浅拷贝）   | a = \[1]; b = a.copy()     | b 为 \[1]   |
| list.clear()     | 清空列表        | a = \[1]; a.clear()        | \[]        |

**实例**：



```python
words = ["banana", "apple", "cherry"]# 排序
words.sort()print(words)  # 输出：["apple", "banana", "cherry"]# 统计
print(words.count("apple"))  # 输出：1# 复制与清空
words_copy = words.copy()
words.clear()print(words)       # 输出：[]
print(words_copy)  # 输出：["apple", "banana", "cherry"]
```

#### Python3 元组

元组与列表类似，但**元素不可修改**，用小括号 `()` 定义，是不可变序列。

##### 元组的创建

用逗号分隔元素，可加括号（也可省略），空元组直接用 `()`：

**实例**：



```python
# 普通元组
t1 = (10, "苹果", True)
t2 = "红", "黄", "蓝"  # 省略括号，仍是元组
print(type(t2))  # 输出：<class 'tuple'># 单元素元组（必须加逗号，否则视为普通括号）
t3 = (5,)  # 正确：元组
t4 = (5)   # 错误：类型为 int
print(type(t3))  # 输出：<class 'tuple'># 空元组
empty_tup = ()
```

##### 访问元组元素

与列表相同，通过索引（正向 `0` 开始，反向 `-1` 开始）或切片访问：

**实例**：



```python
fruits = ("香蕉", "橙子", "葡萄", "芒果")
print(fruits[1])    # 正向索引 → "橙子"
print(fruits[-2])   # 反向索引 → "葡萄"
print(fruits[1:3])  # 切片（左闭右开）→ ("橙子", "葡萄")
print(fruits[:2])   # 从开头到索引1 → ("香蕉", "橙子")
```

##### 元组的不可修改性

元组元素不能直接修改，但可通过**组合**生成新元组：

**实例**：



```python
t1 = (1, 2, 3)
t2 = (4, 5)# 以下操作非法（元组不可修改）# t1[0] = 0  # 报错：TypeError# 组合生成新元组
t3 = t1 + t2
print(t3)  # 输出：(1, 2, 3, 4, 5)# 重复生成新元组
t4 = t2 * 2
print(t4)  # 输出：(4, 5, 4, 5)
```

##### 删除元组

元组元素不可单独删除，但可用 `del` 语句删除整个元组：

**实例**：



```python
cities = ("北京", "上海", "广州")
print(cities)  # 输出：("北京", "上海", "广州")
del cities
# print(cities)  # 报错：NameError（元组已被删除）
```

##### 元组运算符

支持与列表类似的运算符：

| 运算符   | 描述       | 实例            | 结果           |
| ----- | -------- | ------------- | ------------ |
| +     | 组合元组     | (1,2) + (3,4) | (1, 2, 3, 4) |
| \*    | 重复元素     | (1,) \* 3     | (1, 1, 1)    |
| in    | 判断元素是否存在 | 2 in (1,2,3)  | true         |
| len() | 计算长度     | len((1,2,3))  | 3            |

**实例**：

```python
a = (10, 20)
b = (30, 40)
print(a + b)        # 输出：(10, 20, 30, 40)
print(a * 2)        # 输出：(10, 20, 10, 20)
print(20 in a)      # 输出：True
print(len(b))       # 输出：2
```

##### 元组内置函数

| 函数          | 描述            | 实例              | 结果        |
| ----------- | ------------- | --------------- | --------- |
| max(tuple)  | 返回最大值（元素需可比较） | max((5, 2, 8))  | 8         |
| min(tuple)  | 返回最小值         | min((5, 2, 8))  | 2         |
| tuple(iter) | 将可迭代对象转为元组    | tuple(\[1,2,3]) | (1, 2, 3) |

**实例**：



```python
nums = (3, 1, 4, 2)
print(max(nums))  # 输出：4
print(min(nums))  # 输出：1# 列表转元组
lst = ["a", "b"]
t = tuple(lst)
print(t)  # 输出：("a", "b")
```

##### 元组的不可变本质

元组的 “不可变” 指**元素的内存地址不可变**，若元素是可变对象（如列表），其内部可修改：

**实例**：



```python
# 元组包含列表（可变元素）
t = (1, [2, 3], 4)
t[1].append(5)  # 修改列表内部元素（允许）
print(t)  # 输出：(1, [2, 3, 5], 4)
```

元组适合存储不希望被修改的数据，如配置信息、固定序列等，因其不可变性，比列表更节省内存且更安全。

### 第四天：常用数据结构（二）与控制流

#### Python3 字典

字典是可变容器模型，以**键值对（key=>value）** 存储数据，用花括号 `{}` 定义，格式为：`{key1: value1, key2: value2, ...}`。

##### 字典的创建

通过键值对直接定义，或用 `dict()` 函数创建：

**实例**：



```python
# 直接定义（键唯一，值可重复）
student = {"name": "张三","age": 18,"gender": "男"}# 用 dict() 函数创建
fruit = dict(name="苹果", color="红色", price=5.8)# 空字典
empty_dict = {}
empty_dict2 = dict()
```

**注意**：

* 键（key）必须唯一，重复赋值会覆盖前值；

* 键必须是**不可变类型**（如字符串、数字、元组），列表等可变类型不能作为键。

##### 访问字典的值

通过键（`dict[key]`）或 `get()` 方法访问，后者在键不存在时返回默认值（避免报错）：

**实例**：



```python
book = {"title": "Python入门", "author": "李四", "price": 39.9}# 用键访问
print(book["title"])  # 输出：Python入门# 用 get() 方法（推荐）
print(book.get("author"))       # 输出：李四
print(book.get("publisher", "未知"))  # 键不存在，返回默认值：未知
```

**注意**：若用 `dict[key]` 访问不存在的键，会报错 `KeyError`。

##### 修改字典

支持添加新键值对、修改已有值、删除键值对等操作：

**实例**：



```python
car = {"brand": "丰田", "color": "白色"}# 添加新键值对
car["price"] = 200000
print(car)  # 输出：{"brand": "丰田", "color": "白色", "price": 200000}# 修改已有值
car["color"] = "黑色"
print(car)  # 输出：{"brand": "丰田", "color": "黑色", "price": 200000}# 删除键值对（del 语句）
del car["price"]
print(car)  # 输出：{"brand": "丰田", "color": "黑色"}# 清空字典（clear() 方法）
car.clear()
print(car)  # 输出：{}
```

##### 字典的常用操作与运算符

| 操作 / 函数       | 描述            | 实例                  | 结果                       |
| ------------- | ------------- | ------------------- | ------------------------ |
| len(dict)     | 计算键值对数量       | len({"a":1, "b":2}) | 2                        |
| key in dict   | 判断键是否存在       | "a" in {"a":1}      | true                     |
| dict.keys()   | 获取所有键（视图对象）   | {"a":1}.keys()      | dict\_keys(\['a'])       |
| dict.values() | 获取所有值（视图对象）   | {"a":1}.values()    | dict\_values(\[1])       |
| dict.items()  | 获取所有键值对（元组形式） | {"a":1}.items()     | dict\_items(\[('a', 1)]) |

**实例**：



```python
phone = {"brand": "华为", "model": "Mate 60", "price": 6999}
print(len(phone))  # 输出：3
print("model" in phone)  # 输出：True# 遍历键值对
for k, v in phone.items():print(f"{k}: {v}")# 输出：# brand: 华为# model: Mate 60# price: 6999
```

##### 字典内置方法

| 方法                            | 描述                | 实例                                | 结果                     |
| ----------------------------- | ----------------- | --------------------------------- | ---------------------- |
| dict.copy()                   | 复制字典（浅拷贝）         | d = {"a":1}; d2 = d.copy()        | d2 为 {"a":1}           |
| dict.pop(key)                 | 删除键并返回对应值         | d = {"a":1}; d.pop("a")           | 1                      |
| dict.setdefault(key, default) | 获取值，若键不存在则添加并设默认值 | d = {"a":1}; d.setdefault("b", 2) | 2（d 变为 {"a":1, "b":2}） |
| dict.update(dict2)            | 合并字典（覆盖重复键）       | d = {"a":1}; d.update({"b":2})    | d 变为 {"a":1, "b":2}    |

**实例**：



```python
# 合并字典
d1 = {"name": "小明", "age": 12}
d2 = {"age": 13, "gender": "男"}
d1.update(d2)  # 重复键 "age" 被覆盖
print(d1)  # 输出：{"name": "小明", "age": 13, "gender": "男"}# 弹出键值对
d = {"a": 1, "b": 2}
val = d.pop("a")
print(val)  # 输出：1
print(d)    # 输出：{"b": 2}
```

字典适合存储具有映射关系的数据（如用户信息、配置参数等），通过键快速访问值，效率高于列表。

#### Python3 集合

集合（set）是**无序且元素唯一**的容器，支持交集、并集等数学集合操作，用大括号 `{}` 或 `set()` 函数创建。

##### 集合的创建

* 用 `{}` 直接定义（元素用逗号分隔）；

* 用 `set()` 函数从可迭代对象（如列表、字符串）转换；

* 空集合必须用 `set()`（`{}` 表示空字典）。

**实例**：



```python
# 直接创建（自动去重）
fruits = {"苹果", "香蕉", "橙子", "苹果"}
print(fruits)  # 输出：{'苹果', '香蕉', '橙子'}（顺序可能不同）# 从列表创建
nums = set([1, 2, 3, 2])
print(nums)  # 输出：{1, 2, 3}# 空集合
empty_set = set()
```

##### 集合的基本操作

1. 添加元素

* `add(x)`：添加单个元素（已存在则忽略）；

* `update(iter)`：添加可迭代对象中的多个元素（如列表、元组）。

**实例**：

python

运行

```python
colors = {"红", "绿"}# 添加单个元素
colors.add("蓝")
print(colors)  # 输出：{'红', '绿', '蓝'}# 添加多个元素（列表）
colors.update(["黄", "紫"])
print(colors)  # 输出：{'红', '绿', '蓝', '黄', '紫'}（顺序随机）
```

* 移除元素

- `remove(x)`：删除指定元素（不存在则报错）；

- `discard(x)`：删除指定元素（不存在则忽略）；

- `pop()`：随机删除并返回一个元素（集合为空则报错）。

**实例**：



```python
shapes = {"圆形", "方形", "三角形"}

shapes.remove("方形")
print(shapes)  # 输出：{'圆形', '三角形'}

shapes.discard("菱形")  # 元素不存在，无操作
print(shapes)  # 输出：{'圆形', '三角形'}

removed = shapes.pop()
print(removed)  # 输出：圆形（或三角形，随机）
print(shapes)   # 剩余元素：{'三角形'}（或{'圆形'}）
```

* 其他基础操作

| 操作 / 函数   | 描述       | 实例                   | 结果         |
| --------- | -------- | -------------------- | ---------- |
| len(s)    | 计算元素个数   | len({"a", "b"})      | 2          |
| x in s    | 判断元素是否存在 | "a" in {"a", "b"}    | true       |
| s.clear() | 清空集合     | s = {1,2}; s.clear() | s 变为 set() |

**实例**：



```python
letters = {"a", "b", "c"}
print(len(letters))  # 输出：3
print("d" in letters)  # 输出：False

letters.clear()
print(letters)  # 输出：set()
```

##### 集合的运算（交集、并集等）

假设有集合 `a = {1, 2, 3, 4}`，`b = {3, 4, 5, 6}`：

| 运算   | 描述               | 符号 / 方法                            | 结果             |                    |
| ---- | ---------------- | ---------------------------------- | -------------- | ------------------ |
| 并集   | 所有元素（去重）         | \`a                                | b或a.union(b)\` | {1, 2, 3, 4, 5, 6} |
| 交集   | 共同元素             | a & b 或 a.intersection(b)          | {3, 4}         |                    |
| 差集   | a 有而 b 没有的元素     | a - b 或 a.difference(b)            | {1, 2}         |                    |
| 对称差集 | 不同时存在于 a 和 b 的元素 | a ^ b 或 a.symmetric\_difference(b) | {1, 2, 5, 6}   |                    |

**实例**：



```python
a = {1, 2, 3, 4}
b = {3, 4, 5, 6}
print(a | b)  # 并集 → {1, 2, 3, 4, 5, 6}
print(a & b)  # 交集 → {3, 4}
print(a - b)  # 差集 → {1, 2}
```

##### 集合推导式

类似列表推导式，可快速生成集合：

**实例**：



```python
# 生成10以内的偶数集合
even_nums = {x for x in range(10) 
if x % 2 == 0}
print(even_nums)  # 输出：{0, 2, 4, 6, 8}
```

集合适合用于去重、判断元素是否存在，以及执行集合运算（如筛选两个列表的共同元素），因其无序性，不支持索引访问。

#### Python3 条件控制

条件语句根据判断结果（`True` 或 `False`）决定执行的代码块，核心语法为 `if-elif-else`，Python 3.10+ 还支持 `match-case` 结构。

##### if 语句基础

语法格式：





```python
if 条件1:
    代码块1  # 条件1为True时执行
 elif 条件2:
    代码块2  # 条件1为False，条件2为True时执行
 else:
    代码块3  # 所有条件都为False时执行
```

> **注意**：

* 条件后必须加冒号 `:`；

* 代码块通过缩进（通常 4 个空格）区分；

* `elif` 是 `else if` 的简写，可省略或多个。

**实例（判断成绩等级）**：



```python
score = 85
if score >= 90:
    print("优秀")
elif score >= 80:
    print("良好")
elif score >= 60:
    print("及格")
 else:
     print("不及格")# 输出：良好
```

##### 条件判断中的运算符

常用比较运算符：`<`（小于）、`<=`（小于等于）、`>`（大于）、`>=`（大于等于）、`==`（等于）、`!=`（不等于）。

**实例（判断奇偶）**：



```python
num = 7
if num % 2 == 0:
    print(f"{num}是偶数")
else:
    print(f"{num}是奇数")# 输出：7是奇数
```

##### if 嵌套

在一个条件语句内部再包含条件语句，用于多层判断。

**实例（判断数字特性）**：



```python
n = 12
if n > 0:
    print("正数")
    if n % 4 == 0:
        print("且能被4整除")
    else:
        print("但不能被4整除")
 else:
     print("非正数")# 输出：# 正数# 且能被4整除
```

##### match-case 语句（Python 3.10+）

类似其他语言的 `switch-case`，用于多值匹配，简化连续 `elif` 判断。



运行

```python
match 变量:
        case 值1:
        代码块1
        case 值2|值3:  # 多值匹配（用|分隔）
        代码块2
        case _:  # 匹配所有未命中的情况（类似default）
        代码块3
```

**实例（判断星期）**：



```python
weekday = 3
match weekday:
    case 1:print("星期一")
    case 2:print("星期二")
    case 3:print("星期三")
    case 6|7:print("周末")
    case _:
    print("无效数字")# 输出：星期三
```

条件语句是控制程序流程的核心，可根据实际场景选择 `if-elif-else` 或 `match-case`，使逻辑更清晰。

#### Python3 循环语句

Python 提供 `while` 和 `for` 两种循环语句，用于重复执行代码块，可配合 `break`、`continue` 等控制循环流程。

##### while 循环

根据条件重复执行代码，条件为 `True` 时持续运行，直到条件为 `False` 终止。

**基本语法**：





```python
while 条件:
    循环体  # 条件为True时执行
else:
    结束块  # 条件为False时执行（可选）
```

**实例 1：计算 1 到 5 的和**



```python
total = 0
i = 1
while i <= 5:
    total += i
    i += 1  # 避免无限循环
    print("总和：", total)  # 输出：总和：15
```

**实例 2：带 else 的循环**



```python
count = 0
while count < 3:
    print("计数：", count)
    count += 1
else:
    print("计数结束")  # 条件不满足时执行# 输出：# 计数：0# 计数：1# 计数：2# 计数结束
```

**无限循环**：条件永远为 `True` 时触发，需用 `break` 手动终止（如 `Ctrl+C`）：



```python
# 简单的无限循环（谨慎运行）# while True:#     print("循环中...")
```

##### for 循环

用于遍历可迭代对象（如列表、字符串、`range()` 等），依次获取元素执行循环体。

**基本语法**：



```python
for 变量 in 可迭代对象:
    循环体
else:
    结束块  # 遍历完成后执行（可选，break终止时不执行）
```

**实例 1：遍历列表**



```python
fruits = ["苹果", "香蕉", "橙子"]
for fruit in fruits:
    print(fruit)# 输出：# 苹果# 香蕉# 橙子
```

**实例 2：使用 range () 生成数字序列**



```python
# range(开始, 结束, 步长)，左闭右开
for num in range(2, 10, 2):  # 2,4,6,8
    print(num)# 输出：# 2# 4# 6# 8
```

**实例 3：for-else 结构**



```python
for x in range(3):
    print(x)
else:
    print("循环结束")  # 遍历完成后执行# 输出：# 0# 1# 2# 循环结束
```

##### 循环控制语句

* **break**：立即终止当前循环，跳出循环体；

* **continue**：跳过当前循环的剩余代码，直接进入下一轮；

* **pass**：空语句，仅作为占位符，不执行任何操作。

**实例 1：break 终止循环**



```python
for num in range(10):
    if num == 5:
        break  # 遇到5就停止
        print(num)# 输出：0 1 2 3 4（每行一个）
```

**实例 2：continue 跳过当前轮**



```python
for num in range(5):
    if num == 2:
        continue  # 跳过2
        print(num)# 输出：0 1 3 4（每行一个）
```

**实例 3：pass 占位**



```python
for letter in "abc":
    if letter == "b":
        pass  # 暂不处理，保持结构完整
     else:
         print(letter)# 输出：a c（每行一个）
```

循环是处理重复任务的核心工具，`while` 适合未知循环次数的场景，`for` 适合遍历已知序列的场景，灵活使用控制语句可优化循环逻辑。

### 第五天：进阶语法与函数

#### Python3 编程第一步

通过简单实例快速上手 Python 基础语法，涵盖输出、变量、运算、列表、循环和条件判断等核心知识点。

##### 打印字符串

用 `print()` 函数输出文本，直接将字符串放在括号中：

```python
print("Hello, Python!")  # 输出：Hello, Python!
print('编程很有趣')        # 输出：编程很有趣（单引号也可）
```

##### 输出变量值

定义变量并打印，变量无需声明类型，直接赋值即可：



```python
age = 20
score = 95.5
print("年龄：", age)    # 输出：年龄：20
print("分数：", score)  # 输出：分数：95.5
```

##### 变量与数学运算

变量可直接参与算术运算，支持 `+`、`-`、`*`、`/` 等：

```python
a = 15
b = 4
sum_ab = a + b
product_ab = a * b
print("和：", sum_ab)      # 输出：和：19
print("积：", product_ab)  # 输出：积：60
print("商：", a / b)       # 输出：商：3.75
```

##### 列表操作

列表用 `[]` 定义，通过索引访问元素（索引从 `0` 开始）：



```python
pets = ["猫", "狗", "兔子"]
print(pets[0])  # 输出第一个元素：猫
print(pets[2])  # 输出第三个元素：兔子# 遍历列表
for pet in pets:
print(pet)# 输出：# 猫# 狗# 兔子
```

##### for 循环打印数字

用 `range()` 生成数字序列，配合 `for` 循环遍历：



```python
# range(5) 生成 0~4 的数字for num in range(5):print("数字：", num)# 输出：# 数字：0# 数字：1# 数字：2# 数字：3# 数字：4
```

##### 条件判断

用 `if-else` 根据条件执行不同代码块：



```python
num = 7if num % 2 == 0:print(num, "是偶数")else:print(num, "是奇数")# 输出：7 是奇数
```

##### 斐波那契数列

斐波那契数列中，每个数是前两个数的和，用 `while` 循环实现：



```python
# 初始值：a=0，b=1
a, b = 0, 1# 输出小于 50 的斐波那契数
while b < 50:
    print(b)
    a, b = b, a + b  # 同时更新 a 和 b（a 变为原来的 b，b 变为原来的 a+b）# 输出：# 1# 1# 2# 3# 5# 8# 13# 21# 34
```

##### end 关键字

`print()` 中用 `end` 参数指定输出结尾（默认是换行 `\n`）：

python

运行

```python
# 用逗号分隔输出，不换行
a, b = 0, 1
while b < 20:
    print(b, end=', ')
    a, b = b, a + b
# 输出：1, 1, 2, 3, 5, 8, 13, 
```

这些实例覆盖了 Python 基础编程的核心场景，多练习即可快速掌握基本用法。

#### Python 推导式

推导式是一种简洁的语法，用于从现有序列快速生成新的数据结构（列表、字典、集合、元组），核心是 “表达式 + 循环 + 条件” 的组合。

##### 列表推导式

用 `[]` 包裹，格式：`[表达式 for 变量 in 序列 if 条件]`，直接生成新列表。

**实例 1：生成偶数列表**



```python
# 生成10以内的偶数
evens = [x for x in range(10) if x % 2 == 0]
print(evens)  # 输出：[0, 2, 4, 6, 8]
```

**实例 2：处理字符串列表**



```python
words = ["apple", "Banana", "cherry", "Date"]# 提取长度大于5的单词，并转为小写
long_words = [word.lower() for word in words if len(word) > 5]
print(long_words)  # 输出：["banana", "cherry"]
```

##### 字典推导式

用 `{}` 包裹，格式：`{键表达式: 值表达式 for 变量 in 序列 if 条件}`，生成新字典。

**实例 1：键值互换**



```python
original = {"a": 1, "b": 2, "c": 3}# 原字典的键作为值，值作为键
swapped = {v: k for k, v in original.items()}
print(swapped)  # 输出：{1: 'a', 2: 'b', 3: 'c'}
```

**实例 2：过滤并生成新字典**



```python
numbers = [1, 2, 3, 4, 5]# 生成键为数字，值为数字平方的字典（仅保留偶数）
square_dict = {x: x**2 for x in numbers if x % 2 == 0}
print(square_dict)  # 输出：{2: 4, 4: 16}
```

##### 集合推导式

用 `{}` 包裹，格式：`{表达式 for 变量 in 序列 if 条件}`，生成去重的新集合。

**实例 1：提取唯一字符**



```python
text = "hello world"# 提取所有非空格的唯一字符
unique_chars = {c for c in text if c != " "}
print(unique_chars)  # 输出：{'h', 'e', 'l', 'o', 'w', 'r', 'd'}
```

**实例 2：生成平方数集合**



```python
# 生成1~5的平方数，自动去重（此处无重复）
squares = {x**2 for x in range(1, 6)}
print(squares)  # 输出：{1, 4, 9, 16, 25}
```

##### 元组推导式（生成器表达式）

用 `()` 包裹，格式：`(表达式 for 变量 in 序列 if 条件)`，返回**生成器对象**（需用 `tuple()` 转换为元组）。

**实例 1：生成数字元组**



```python
# 推导式返回生成器
gen = (x * 2 for x in range(3))# 转换为元组
doubles = tuple(gen)
print(doubles)  # 输出：(0, 2, 4)
```

**实例 2：过滤数据**



```python
# 生成10以内能被3整除的数字的生成器
filtered_gen = (x for x in range(10) if x % 3 == 0)print(tuple(filtered_gen))  # 输出：(0, 3, 6, 9)
```

推导式的优势是用一行代码完成循环 + 条件 + 生成的逻辑，使代码更简洁，但需注意避免过于复杂的表达式，以免降低可读性。

#### Python3 迭代器与生成器

迭代器和生成器是 Python 中处理迭代的重要工具，用于高效遍历数据，尤其适合处理大量或动态生成的数据。

##### 迭代器

迭代器是一个可记住遍历位置的对象，只能向前访问，不能后退。通过 `iter()` 函数创建，用 `next()` 函数获取下一个元素。

###### 基本使用



```python
# 从列表创建迭代器
nums = [10, 20, 30]
it = iter(nums)# 用 next() 获取元素
print(next(it))  # 输出：10
print(next(it))  # 输出：20# 用 for 循环遍历（更常用）
for num in it:
    print(num)  # 输出：30（注意：前面已取2个，这里从第三个开始）
```

###### 迭代器的终止

当元素耗尽时，`next()` 会抛出 `StopIteration` 异常，需用 `try-except` 捕获：



```python
it = iter([1, 2])
try:
    print(next(it))  # 1
    print(next(it))  # 2
    print(next(it))  # 无元素，触发异常
 except StopIteration:
      print("迭代结束")
```

##### 自定义迭代器

通过类实现 `iter()` 和 `next()` 方法，可创建自定义迭代器：

* `iter()`：返回迭代器对象自身；

* `next()`：返回下一个元素，无元素时抛出 `StopIteration`。

**实例：生成 1\~5 的迭代器**



```python
class MyIterator:def __init__(self):
        self.current = 1  # 初始值
        def __iter__(self):
            return self  # 返回自身
        def __next__(self):
            if self.current > 5:
                raise StopIteration  # 终止条件
        value = self.current
        self.current += 1
        return value

# 使用自定义迭代器
my_iter = MyIterator()
for num in my_iter:
    print(num)  # 输出：1 2 3 4 5（每行一个）
```

##### 生成器

生成器是一种特殊的迭代器，由带 `yield` 的函数定义，调用时返回迭代器，可逐步产生值（节省内存）。

###### 基本使用



```python
def my_generator():
    yield 1  # 第一次调用返回1，暂停
    yield 2  # 第二次调用返回2，暂停
    yield 3  # 第三次调用返回3，结束# 创建生成器（迭代器）
gen = my_generator()
print(next(gen))  # 输出：1
print(next(gen))  # 输出：2
for val in gen:
    print(val)  # 输出：3
```

###### 生成器的优势

无需一次性存储所有数据，适合大数据或无限序列：



```python
# 生成无限偶数序列（仅示例，实际使用需限制终止条件）
def even_numbers():
    n = 0while True:yield n
        n += 2

even_gen = even_numbers()
print(next(even_gen))  # 0
print(next(even_gen))  # 2
print(next(even_gen))  # 4
```

###### 斐波那契数列生成器



```python
def fibonacci(max_count):
    a, b = 0, 1
    count = 0
    while count < max_count:
        yield a  # 返回当前值
        a, b = b, a + b  # 更新下一组值
        count += 1# 生成前6个斐波那契数
fib_gen = fibonacci(6)
for num in fib_gen:
    print(num, end=" ")  # 输出：0 1 1 2 3 5
```

迭代器和生成器简化了迭代逻辑，生成器尤其适合处理大量数据或动态生成序列，避免内存占用过高。

#### Python with 关键字

with 语句是 Python 中用于**资源管理**的优雅语法，尤其适合处理文件、数据库连接等需要手动释放的资源，能自动完成资源的创建与清理。

##### 为什么需要 with 语句？

传统资源管理（如文件操作）需手动关闭资源，易出现遗漏或代码冗余：



```python
# 传统方式：需手动 close()
file = open("data.txt", "r")
try:
    content = file.read()finally:
    file.close()  # 必须手动关闭，否则可能资源泄露
```

with 语句的优势：

* **自动释放资源**：无需手动调用 `close()` 等方法；

* **代码简洁**：减少 `try-finally` 样板代码；

* **异常安全**：即使代码块中发生异常，资源也会被正确清理。

##### with 语句的基本语法



```python
with 表达式 as 变量:# 资源使用代码块（变量为表达式返回的资源对象）
```

* 表达式返回一个支持**上下文管理协议**的对象（需实现 `enter()` 和 `exit()` 方法）；

* 代码块执行完毕后，自动调用对象的清理方法（如关闭文件）。

##### 常用场景示例

1. 文件操作（最典型应用）



```python
# 读取文件
with open("note.txt", "r", encoding="utf-8") as f:
    lines = f.readlines()  # 读取所有行
    for line in lines:
        print(line.strip())  # 处理内容# 写入文件
        with open("output.txt", "w") as f:
            f.write("Hello, with!")  # 写入内容# 代码块结束后，文件自动关闭，无需手动操作
```

* 同时管理多个资源

可在一个 with 语句中管理多个资源（用逗号分隔）：



```python
# 同时打开两个文件（读和写）
with open("source.txt", "r") as src, open("dest.txt", "w") as dst:
    content = src.read()  # 从源文件读取
    dst.write(content)    # 写入目标文件
```

* 数据库连接

以 SQLite 为例，用 with 管理数据库连接，自动提交或回滚事务：



```python
import sqlite3

# 连接数据库，自动关闭连接
with sqlite3.connect("test.db") as conn:
    cursor = conn.cursor()
    cursor.execute("CREATE TABLE IF NOT EXISTS users (id INT, name TEXT)")
    cursor.execute("INSERT INTO users VALUES (1, '张三')")
    conn.commit()  # 提交事务
```

* 线程锁（确保线程安全）



```python
import threading

lock = threading.Lock()# 自动获取和释放锁，避免死锁
with lock:# 临界区代码（多线程环境下安全执行）
    print("线程安全的操作")
```

##### 上下文管理协议原理

with 语句依赖对象实现以下两个方法：

1. `enter()`：进入上下文时调用，返回的对象赋值给 `as` 后的变量；

2. `exit()`：退出上下文时调用（无论是否发生异常），负责资源清理。

**自定义上下文管理器示例（计时器）**：



```python
import time

class Timer:def __enter__(self):
        self.start = time.time()  # 记录开始时间
        return self  # 返回自身给 as 变量
        def __exit__(self, exc_type, exc_val, exc_tb):
            self.end = time.time()  # 记录结束时间
            print(f"耗时：{self.end - self.start:.2f}秒")# 返回 False 表示不抑制异常（如需捕获异常，可在此处理）
            return False# 使用自定义上下文管理器with Timer() as t:# 模拟耗时操作
            sum(range(10000000))  # 计算 0~9999999 的和
```

##### 用 contextlib 简化自定义上下文

`contextlib` 模块的 `@contextmanager` 装饰器可快速创建上下文管理器（无需定义类）：



```python
from contextlib import contextmanager

@contextmanager
def log_operation(operation):
    print(f"开始：{operation}")
    yield  # 暂停，执行 with 块中的代码
    print(f"结束：{operation}")# 使用
    with log_operation("数据备份"):
        print("正在备份...")  # 模拟备份操作# 输出：# 开始：数据备份# 正在备份...# 结束：数据备份
```

##### 最佳实践

* 处理文件、网络连接、数据库等资源时，**优先使用 with 语句**；

* 单个 with 语句可管理多个资源（用逗号分隔），减少嵌套；

* 自定义上下文管理器时，明确 `exit()` 中是否需要处理异常（返回 `True` 表示抑制异常）。

with 语句通过简洁的语法解决了资源管理的复杂性，是编写健壮 Python 代码的重要工具。

#### Python3 函数

函数是可重复使用的代码块，用于实现单一或关联功能，能提高代码复用性和模块性。除了 Python 内置函数（如 `print()`），还可自定义函数。

##### 定义函数

用 `def` 关键字定义函数，语法：



```python
def 函数名(参数列表):"""函数文档字符串（可选）"""
    函数体（缩进）
    return 表达式  # 可选，返回结果
```

**实例 1：简单函数**



```python
def greet():"""输出问候语"""
print("Hello, 函数！")# 调用函数
greet()  # 输出：Hello, 函数！
```

**实例 2：带参数和返回值的函数**



```python
def add(a, b):"""返回两个数的和"""
    return a + b

result = add(3, 5)
print(result)  # 输出：8
```

##### 参数传递

Python 中参数传递分为**不可变对象**（如整数、字符串、元组）和**可变对象**（如列表、字典）：

* 不可变对象：传递值的副本，函数内修改不影响外部；

* 可变对象：传递引用，函数内修改会影响外部。

**实例 1：传递不可变对象（整数）**



```python
def modify_num(x):
    x = 10  # 函数内修改，不影响外部
    print("函数内：", x)

num = 5
modify_num(num)
print("函数外：", num)  # 输出：5（外部未变）
```

**实例 2：传递可变对象（列表）**



```python
def add_item(lst):
    lst.append("new")  # 函数内修改，影响外部
    print("函数内：", lst)

my_list = [1, 2]
add_item(my_list)
print("函数外：", my_list)  # 输出：[1, 2, 'new']（外部已变）
```

##### 参数类型

1. 必需参数

必须按顺序传入，数量与声明一致，否则报错：



```python
def print_name(name):
    print("姓名：", name)

print_name("张三")  # 正确# print_name()  # 错误：缺少参数
```

* 关键字参数

通过参数名指定值，可忽略顺序：



```python
def introduce(name, age):
print(f"我叫{name}，今年{age}岁")# 用关键字参数调用，顺序可换
introduce(age=20, name="李四")  # 输出：我叫李四，今年20岁
```

* 默认参数

参数指定默认值，调用时可省略：



```python
def power(base, exp=2):"""计算 base 的 exp 次方，默认平方"""
    return base ** exp

print(power(3))    # 省略 exp，用默认值 2 → 9
print(power(3, 3)) # 传入 exp → 27
```

* 不定长参数

处理不确定数量的参数，分两种：

* `*args`：接收多个位置参数，打包为元组；

* `**kwargs`：接收多个关键字参数，打包为字典。

**实例**：



```python
def print_args(arg1, *args, **kwargs):
    print("固定参数：", arg1)
    print("不定长位置参数：", args)  # 元组
    print("不定长关键字参数：", kwargs)  # 字典

print_args(1, 2, 3, name="张三", age=18)# 输出：# 固定参数：1# 不定长位置参数：(2, 3)# 不定长关键字参数：{'name': '张三', 'age': 18}
```

##### 匿名函数（lambda）

用 `lambda` 定义简洁的匿名函数，语法：`lambda 参数: 表达式`（返回表达式结果）。

**实例**：



```python
# 定义匿名函数（求两数之和）
add = lambda x, y: x + y
print(add(2, 3))  # 输出：5# 结合默认参数
multiply = lambda a, b=2: a * b
print(multiply(3))  # 输出：6（3*2）
```

##### return 语句

用于结束函数并返回结果，无 `return` 则默认返回 `None`。

**实例**：



```python
def divide(a, b):if b == 0:
    return "除数不能为0"  # 返回字符串
    return a / b  # 返回除法结果
    print(divide(6, 2))   # 输出：3.0
    print(divide(6, 0))   # 输出：除数不能为0
```

##### 强制位置参数（Python 3.8+）

用 `/` 分隔，左侧参数必须用位置传递，不能用关键字：



```python
def func(a, b, /, c, d):
    print(a, b, c, d)

func(1, 2, 3, 4)  # 正确（a、b 用位置参数）
func(1, 2, c=3, d=4)  # 正确（c、d 可用关键字）# func(a=1, b=2, 3, 4)  # 错误（a、b 不能用关键字）
```

函数是 Python 模块化编程的核心，合理使用不同参数类型和匿名函数，可使代码更灵活、高效。



### 第六天：模块、输入输出与文件操作

#### Python3 模块

模块是封装代码的文件（`.py`），用于实现特定功能；包是模块的集合（含 `init.py` 的目录），用于组织模块结构。二者核心作用是**代码复用**、**避免命名冲突**和**优化代码组织**。

##### 模块的使用

###### 导入模块

通过 `import` 语句导入模块，常用方式：

* `import 模块名`：导入整个模块，通过 “模块名。功能” 调用；

* `from 模块名 import 功能`：导入模块中的指定功能，直接调用；

* `import 模块名 as 别名`：给模块起别名，简化调用。

**实例 1：导入标准库模块（`math`）**



```python
# 导入整个模块
import math
print(math.sqrt(16))  # 调用模块中的函数 → 4.0
print(math.pi)        # 调用模块中的常量 → 3.141592653589793# 导入指定功能
from math import pow, ceil
    print(pow(2, 3))  # 2的3次方 → 8.0
    print(ceil(3.2))  # 向上取整 → 4# 给模块起别名
import math as m
print(m.floor(4.8))  # 向下取整 → 4
```

**实例 2：导入自定义模块**假设自定义模块 `calc.py`（含以下代码）：



```python
# calc.py
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

在其他文件中导入使用：



```python
import calc
print(calc.add(5, 3))      # 输出：8
print(calc.subtract(10, 4))# 输出：6
```

###### 模块搜索路径

Python 按以下顺序查找模块，可通过 `sys.path` 查看：

1. 当前执行脚本所在目录；

2. 环境变量 `PYTHONPATH` 指定的目录；

3. Python 标准库目录。

**实例：查看并添加搜索路径**

python

运行

```python
import sys
# 查看当前搜索路径
print(sys.path)# 添加自定义目录到搜索路径（临时生效）
sys.path.append("D:/my_modules")
```

###### `name` 属性

用于判断模块是 “直接运行” 还是 “被导入”：

* 模块直接运行时，`name == "__main__"`；

* 模块被导入时，`name == 模块名`。

**实例：模块自测试**在 `calc.py` 中添加：

python

运行

```python
if __name__ == "__main__":# 直接运行模块时执行（测试代码）print("模块自测：")print(add(2, 3))  # 输出：5else:# 被导入时执行（可选）print("calc模块被导入")
```

###### &#x20;`dir()` 函数

查看模块中定义的所有功能（函数、变量、类等），返回字符串列表。

**实例**：

python

运行

```python
import math
# 查看math模块的核心功能print(dir(math)[:5])  # 输出前5个：['__doc__', '__loader__', '__name__', '__package__', '__spec__']# 查看当前命名空间的变量/函数print(dir()[:3])  # 输出前3个：['__builtins__', '__doc__', '__name__']
```

##### 常用标准库模块

Python 内置大量实用模块，无需安装即可使用：

| 模块名      | 核心功能              | 实例用法                                  |
| -------- | ----------------- | ------------------------------------- |
| math     | 数学运算              | math.sin(math.pi/2) → 1.0             |
| random   | 生成随机数             | random.randint(1, 10) → 随机整数          |
| datetime | 处理日期时间            | datetime.date.today() → 今日日期          |
| os       | 操作系统交互（文件 / 目录操作） | os.listdir(".") → 列出当前目录文件            |
| sys      | 系统参数与函数（命令行参数等）   | sys.argv → 获取命令行参数列表                  |
| json     | 处理 JSON 数据        | json.dumps({"name": "张三"}) → JSON 字符串 |

##### 包的使用

包是含 `init.py` 文件的目录，用于组织多个相关模块，避免模块名冲突。

###### 包的结构

假设包结构如下：

plaintext

```plain&#x20;text
my_package/          # 顶层包
    __init__.py      # 包初始化文件（空文件或含初始化代码）
    module1.py       # 子模块1
    module2.py       # 子模块2
    sub_package/     # 子包
        __init__.py
        module3.py   # 子包的模块
```

###### 导入包中的模块

* 导入顶层包的模块；

* 导入子包的模块；

* 给包 / 模块起别名。

**实例**：



```python
# 导入顶层包的模块
from my_package import module1
print(module1.func1())  # 调用module1中的func1# 导入子包的模块
from my_package.sub_package import module3
print(module3.func3())  # 调用module3中的func3# 起别名
from my_package import module2 as m2
print(m2.func2())  # 调用module2中的func2
```

###### `init.py` 文件的作用

* 标识目录为 Python 包；

* 初始化包（如定义 `all` 变量，控制 `from 包 import *` 的导入内容）。

**实例**：在 `my_package/__init__.py` 中定义 `all`：



```python
# my_package/__init__.py
__all__ = ["module1", "module2"]  # 限制from my_package import * 仅导入这两个模块
```

> ##### 最佳实践

1. **优先使用标准库模块**：避免重复造轮子，标准库模块稳定性高；

2. **模块命名规范**：模块名用小写字母，多个单词用下划线分隔（如 `user_utils.py`）；

3. **避免 `from 模块 import *`**：易导致命名冲突，推荐导入指定功能；

4. **包结构清晰**：按功能划分模块到不同包，如 `utils/` 放工具函数，`models/` 放数据模型。



#### Python name 与 \_\_main\_\_

#####

`name` 是 Python 的内置变量，用于标识模块的运行状态；`main` 是一个特殊字符串，标识模块作为主程序运行。二者结合可控制代码在 “直接运行” 和 “被导入” 时的不同行为。

##### `name` 变量的含义

`name` 的值由模块的使用方式决定：

* **模块直接运行**（如 `python script.py`）：`name` 被自动设为 `"__main__"`；

* **模块被导入**（如 `import script`）：`name` 被设为模块的文件名（不含 `.py` 后缀）。

**实例**：创建 `demo.py` 文件



```python
# demo.pyprint(f"当前 __name__ 的值：{__name__}")
```

* **直接运行 `demo.py`**：

* bash

```bash
python demo.py
# 输出：当前 __name__ 的值：__main__
```

* **在其他文件中导入 `demo.py`**：

*

```python
# test.pyimport demo  # 导入模块
```

* 运行 `test.py` 输出：



```bash
当前 __name__ 的值：demo  # __name__ 为模块名
```

##### `if name == "__main__":` 的作用

该语句用于区分模块的两种运行场景，实现 “**脚本独立运行时执行特定代码，被导入时不执行**”。

**实例**：优化 `demo.py`

python

运行

```python
# demo.pydef add(a, b):return a + b

# 测试代码（仅在直接运行时执行）if __name__ == "__main__":print("模块正在直接运行")print("3 + 5 =", add(3, 5))  # 输出：3 + 5 = 8else:print("模块被导入使用")
```

* **直接运行 `demo.py`**：



```bash
python demo.py
# 输出：# 模块正在直接运行# 3 + 5 = 8
```

* **在 `test.py` 中导入 `demo.py`**：



```python
# test.pyimport demo
print("10 + 20 =", demo.add(10, 20))  # 调用模块函数
```

* 运行 `test.py` 输出：

```bash
模块被导入使用
10 + 20 = 30  # 仅执行导入后的调用，不执行测试代码
```

> 实际应用场景

* **模块自测**：在模块中编写测试代码，直接运行时执行测试，被导入时不干扰其他程序；

* **脚本入口**：作为程序的主入口，如 `main()` 函数仅在直接运行时调用；

* **避免副作用**：防止模块被导入时自动执行耗时操作（如文件读写、网络请求）。

**实例：主程序入口**



```python
# calculator.py
def multiply(x, y):
    return x * y

def main():print("计算器程序")
    print("2 * 3 =", multiply(2, 3))
if __name__ == "__main__":
    main()  # 仅直接运行时执行主函数
```

> ##### 总结

* `name` 反映模块的运行状态：直接运行时为 `"__main__"`，被导入时为模块名；

* `if name == "__main__":` 是 Python 中 “**代码复用与独立运行兼顾**” 的经典写法，使模块既可以被其他程序导入使用，也能作为独立脚本运行。

#### Python3 输入和输出



Python 提供了丰富的输入输出方式，包括控制台输出格式化、键盘输入读取以及文件读写操作，同时支持对象的持久化存储。

##### 输出格式美化

通过多种方式控制输出格式，使结果更易读。

1. 字符串格式化方法

* **`str.format()`**：灵活的占位符格式化，支持位置、关键字参数和格式控制。



```python
# 位置参数
print("姓名：{0}，年龄：{1}".format("张三", 20))  # 输出：姓名：张三，年龄：20# 关键字参数
print("身高：{height}cm，体重：{weight}kg".format(height=175, weight=65))  # 输出：身高：175cm，体重：65kg# 格式控制（保留2位小数）
print("圆周率：{:.2f}".format(3.14159))  # 输出：圆周率：3.14
```

* **`f-string`（Python 3.6+）**：更简洁的字面量格式化，直接嵌入变量。



```python
name = "李四"
score = 95.5
print(f"{name}的成绩是{score}分")  # 输出：李四的成绩是95.5分
print(f"成绩四舍五入：{round(score)}")  # 输出：成绩四舍五入：96
```

* **旧式 `%` 格式化**：类似 C 语言的 `printf`，兼容性强但功能有限。



```python
print("年龄：%d，成绩：%.1f" % (18, 92.3))  # 输出：年龄：18，成绩：92.3
```

* 字符串对齐方法

- `rjust(width)`：右对齐，左侧补空格；

- `ljust(width)`：左对齐，右侧补空格；

- `center(width)`：居中对齐，两侧补空格；

- `zfill(width)`：左侧补 0（适合数字）。

python

运行

```python
print("hello".rjust(10))  # 输出：     hello（共10位，右对齐）
print("world".ljust(10))  # 输出：world     （共10位，左对齐）
print("python".center(10))# 输出：  python  （共10位，居中）
print("123".zfill(5))     # 输出：00123（共5位，补0）
```

##### 读取键盘输入

用 `input()` 函数获取用户输入（返回字符串类型）：



```python
name = input("请输入姓名：")
age = int(input("请输入年龄："))  # 转换为整数
print(f"你好，{name}（{age}岁）")
```

**运行示例**：



```plain&#x20;text
请输入姓名：王五
请输入年龄：22
你好，王五（22岁）
```

##### 文件读写操作

通过 `open()` 函数操作文件，需指定文件名和模式，推荐用 `with` 语句自动管理资源。

* 文件打开模式

| 模式 | 描述                     |
| -- | ---------------------- |
| r  | 只读（默认），文件不存在则报错        |
| w  | 只写，覆盖原有内容，文件不存在则创建     |
| a  | 追加，在文件末尾添加内容，文件不存在则创建  |
| r+ | 读写，文件指针在开头             |
| b  | 二进制模式（如 rb、wb，用于非文本文件） |

* 读取文件



```python
# 读取文本文件（推荐 with 语句）
with open("test.txt", "r", encoding="utf-8") as f:
    content = f.read()  # 读取全部内容
    print(content)# 逐行读取
    with open("test.txt", "r") as f:
        for line in f:
            print(line.strip())  # 去除换行符
```

* 写入文件



```python
# 写入内容（覆盖模式）
with open("output.txt", "w") as f:
    f.write("第一行内容\n")
    f.write("第二行内容\n")# 追加内容
    with open("output.txt", "a") as f:
        f.write("追加的内容\n")
```

* 文件指针操作

- `f.tell()`：返回当前指针位置（字节偏移量）；

- `f.seek(offset, whence)`：移动指针，`whence=0`（开头，默认）、`1`（当前位置）、`2`（结尾）。

python

运行

```python
with open("test.txt", "r") as f:
    f.seek(5)  # 从开头移动5个字节
    print(f.read(3))  # 读取3个字符
    print(f.tell())   # 输出当前指针位置
```

##### 对象持久化（`pickle` 模块）

`pickle` 用于序列化（保存）和反序列化（恢复）Python 对象，实现数据持久化。

* 保存对象到文件

python

运行

```python
import pickle

data = {"name": "赵六","hobbies": ["读书", "跑步"],"age": 25}# 序列化并保存with open("data.pkl", "wb") as f:
    pickle.dump(data, f)  # 将对象写入文件
```

* 从文件恢复对象



```python
import pickle

# 反序列化并读取
with open("data.pkl", "rb") as f:
    restored_data = pickle.load(f)  # 从文件恢复对象
    print(restored_data["hobbies"])  # 输出：['读书', '跑步']
```

> ##### 总结

* 输出格式化推荐用 `f-string` 或 `str.format()`，简洁且功能强；

* 读取输入用 `input()`，注意类型转换；

* 文件操作优先用 `with` 语句，自动关闭资源，避免泄露；

* `pickle` 适合保存复杂对象（如字典、列表），但仅能在 Python 中使用。

#### Python3 File(文件) 方法

#####

`open()` 方法是 Python 中处理文件的核心函数，用于打开文件并返回文件对象，后续的读写操作均通过该对象完成。

##### `open()` 方法语法



```python
open(file, mode='r', encoding=None, ...)
```

| 参数       | 说明                                                  |
| -------- | --------------------------------------------------- |
| file     | 必需，文件路径（相对路径或绝对路径，如 "data.txt" 或 "/home/file.txt"）。 |
| mode     | 可选，打开模式（默认 'r'，只读文本模式），详见下表。                        |
| encoding | 可选，文本文件编码（如 'utf-8'，二进制模式无需指定）。                     |

##### 文件打开模式（`mode`）

| 模式 | 描述                                                  |
| -- | --------------------------------------------------- |
| r  | 只读（默认），文件不存在则报错，指针在开头。                              |
| w  | 只写，覆盖原有内容；文件不存在则创建，指针在开头。                           |
| a  | 追加，新内容写在文件末尾；文件不存在则创建，指针在结尾。                        |
| r+ | 读写，指针在开头，可覆盖原有内容。                                   |
| w+ | 读写，覆盖原有内容；文件不存在则创建。                                 |
| a+ | 读写，新内容追加在末尾；文件不存在则创建，读操作需移动指针。                      |
| b  | 二进制模式（与上述模式结合，如 rb 只读二进制，wb 只写二进制），用于非文本文件（图片、音频等）。 |
| x  | 新建文件并写入，文件已存在则报错（如 x、xb）。                           |

##### 文件对象常用方法

文件对象通过 `open()` 创建后，提供以下核心方法操作文件：

| 方法                     | 描述                                                 |
| ---------------------- | -------------------------------------------------- |
| read(size=-1)          | 读取文件内容，size 为字节数（默认读取全部），返回字符串（文本模式）或字节流（二进制模式）。   |
| readline(size=-1)      | 读取一行内容（包括 \n），size 限制最大字节数。                        |
| readlines()            | 读取所有行，返回列表（每行作为元素，包含 \n）。                          |
| write(str)             | 写入字符串（文本模式）或字节流（二进制模式），返回写入的长度。                    |
| writelines(seq)        | 写入字符串列表 seq（需手动添加 \n 换行）。                          |
| seek(offset, whence=0) | 移动指针：offset 为偏移量，whence=0（从开头，默认）、1（从当前位置）、2（从结尾）。 |
| tell()                 | 返回当前指针位置（字节偏移量）。                                   |
| close()                | 关闭文件（必须调用，或用 with 语句自动关闭）。                         |
| flush()                | 立即刷新缓冲区，将数据写入文件（无需等待关闭）。                           |

##### 实例演示

1. 文本文件读写（推荐 `with` 语句自动关闭）

```python
# 写入文件（w 模式）
with open("notes.txt", "w", encoding="utf-8") as f:
    f.write("第一行内容\n")
    f.writelines(["第二行内容\n", "第三行内容\n"])  # 写入列表# 读取文件（r 模式）
    with open("notes.txt", "r", encoding="utf-8") as f:
        print("全部内容：")
        print(f.read())  # 读取全部

    f.seek(0)  # 指针移回开头
    print("\n逐行读取：")
    for line in f:
        print(line.strip())  # 去除换行符
```

* 二进制文件操作（如图片）



```python
# 复制图片（二进制模式）
with open("source.jpg", "rb") as src, open("copy.jpg", "wb") as dst:
    data = src.read()  # 读取二进制数据
    dst.write(data)    # 写入二进制数据
```

* 追加内容（`a` 模式）



```python
with open("log.txt", "a", encoding="utf-8") as f:
import datetime
now = datetime.datetime.now().strftime("%Y-%m-%d %H:%M")
f.write(f"{now}：操作记录\n")  # 追加到文件末尾
```

* 指针操作（`seek()` 和 `tell()`）



```python
with open("test.txt", "r+", encoding="utf-8") as f:
    f.write("abcdef")  # 写入内容
    f.seek(2)  # 指针移到第2个字节（索引从0开始）
    print(f.read(3))  # 从指针位置读取3个字符 → "cde"
    print(f.tell())   # 输出当前指针位置 → 5
```

> ##### 注意事项

1. **编码问题**：文本文件需指定 `encoding`（如 `utf-8`），避免中文乱码；

2. **资源释放**：务必关闭文件，推荐用 `with` 语句（自动调用 `close()`）；

3. **模式选择**：写入时注意 `w`（覆盖）与 `a`（追加）的区别，避免误删数据；

4. **二进制模式**：处理图片、音频等非文本文件时，必须加 `b` 模式（如 `rb`、`wb`）。

通过 `open()` 方法和文件对象的方法，可灵活实现各种文件操作，是 Python 处理持久化数据的基础。



#### Python3 OS 文件/目录方法

#####

`os` 模块是 Python 标准库中用于与操作系统交互的核心模块，支持文件操作、目录管理、环境变量访问等功能，且具有跨平台特性（兼容 Windows、Linux、macOS）。

##### 导入 os 模块

使用前需先导入：



```python
import os
```

##### 常用功能与实例

1. 目录操作

* **获取当前工作目录**：`os.getcwd()`



```python
current_dir = os.getcwd()
print("当前目录：", current_dir)  # 输出：例如 /home/user/project
```

* **切换工作目录**：`os.chdir(path)`

```python
os.chdir("/tmp")  # 切换到 /tmp 目录
print(os.getcwd())  # 输出：/tmp
```

* **列出目录内容**：`os.listdir(path)`（默认当前目录）

```python
items = os.listdir()  # 获取当前目录下的文件和子目录
print("目录内容：", items)  # 输出：['file1.txt', 'dir1', ...]
```

* **创建目录**：`os.mkdir(path)`（单级目录）、`os.makedirs(path)`（多级目录）



```python
os.mkdir("new_dir")  # 创建单级目录
os.makedirs("parent/child")  # 递归创建多级目录（若父目录不存在）
```

* **删除目录**：`os.rmdir(path)`（空目录）、`os.removedirs(path)`（递归删除空目录）



```python
os.rmdir("new_dir")  # 删除空目录
os.removedirs("parent/child")  # 若 child 和 parent 均为空，则递归删除
```

* 文件操作

- **重命名文件 / 目录**：`os.rename(old, new)`



```python
os.rename("old.txt", "new.txt")  # 重命名文件
os.rename("old_dir", "new_dir")  # 重命名目录
```

* **删除文件**：`os.remove(path)`



```python
os.remove("unused.txt")  # 删除指定文件（目录需用 rmdir）
```

* 环境变量

- **获取环境变量**：`os.getenv(key)`



```python
home = os.getenv("HOME")  # Linux/macOS 家目录
user = os.getenv("USER")  # 当前用户名
print("家目录：", home)
```

* **设置环境变量**：`os.environ[key] = value`（临时生效）



```python
os.environ["TEMP_DIR"] = "/tmp/mytemp"  # 设置临时环境变量
```

* 执行系统命令

`os.system(command)`：在系统 shell 中执行命令，返回退出状态码（0 表示成功）。



```python
# Linux/macOS 示例：列出当前目录详细信息
os.system("ls -l")# Windows 示例：列出当前目录# os.system("dir")
```

* 遍历目录树

`os.walk(top)`：递归遍历目录及其子目录，返回 `(root, dirs, files)` 三元组（当前目录路径、子目录列表、文件列表）。

```python
for root, dirs, files in os.walk("."):  # 从当前目录开始遍历
    print(f"目录：{root}")
    print(f"子目录：{dirs}")
    print(f"文件：{files}\n")
```

##### os.path 子模块（路径处理）

`os.path` 提供路径解析、拼接等工具函数，跨平台兼容（自动处理 `/` 和 `\` 差异）。

| 方法                    | 描述          | 实例                              | 结果                  |
| --------------------- | ----------- | ------------------------------- | ------------------- |
| os.path.join(a, b)    | 拼接路径        | os.path.join("dir", "file.txt") | dir/file.txt        |
| os.path.abspath(path) | 获取绝对路径      | os.path.abspath("file.txt")     | /home/user/file.txt |
| os.path.exists(path)  | 判断路径是否存在    | os.path.exists("dir")           | True 或 False        |
| os.path.isfile(path)  | 判断是否为文件     | os.path.isfile("file.txt")      | True 或 False        |
| os.path.isdir(path)   | 判断是否为目录     | os.path.isdir("dir")            | True 或 False        |
| os.path.split(path)   | 分割路径为目录和文件名 | os.path.split("/a/b/c.txt")     | ("/a/b", "c.txt")   |

**实例**：



```python
# 拼接路径并判断是否为文件
file_path = os.path.join("data", "report.csv")
print("完整路径：", os.path.abspath(file_path))
print("是否为文件：", os.path.isfile(file_path))
```

> ##### 注意事项

1. **跨平台兼容**：避免硬编码路径分隔符（如 `/` 或 `\`），优先用 `os.path.join()`；

2. **权限问题**：操作文件 / 目录时需确保有足够权限，否则会抛出 `PermissionError`；

3. **异常处理**：文件操作可能引发多种异常（如 `FileNotFoundError`、`IsADirectoryError`），建议用 `try-except` 捕获。

`os` 模块是处理系统资源的利器，结合 `os.path` 可高效完成文件和目录管理任务。



### 第七天：错误处理与面向对象



#### Python3 错误和异常

在 Python 中，程序运行时可能出现两类问题：**语法错误**（解析错误）和**异常**（运行时错误）。异常可通过代码捕获并处理，确保程序稳健运行。

1. 语法错误

语法错误是代码不符合 Python 语法规则导致的，如缺少冒号、括号不匹配等，解释器会直接报错并指出位置。

**实例**：



```python
# 缺少冒号（语法错误）
if 5 > 3
    print("5大于3")
```

**报错信息**：



```plain&#x20;text
  File "<stdin>", line 1
    if 5 > 3
           ^
SyntaxError: invalid syntax
```

* 异常

即使语法正确，运行时也可能因逻辑错误触发异常（如除以零、变量未定义等）。常见异常类型包括 `ZeroDivisionError`、`NameError`、`TypeError` 等。

**实例**：



```python
# 除以零（运行时异常）
print(10 / 0)  # 触发 ZeroDivisionError
```

**报错信息**：



```plain&#x20;text
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

* 异常处理（`try-except` 语句）

使用 `try-except` 捕获并处理异常，避免程序崩溃。

**基本语法**：



```python
try:# 可能触发异常的代码
except 异常类型1:# 处理异常类型1的代码
except (异常类型2, 异常类型3):# 处理多个异常的代码
else:# 无异常时执行的代码（可选）
finally:# 无论是否有异常都执行的代码（可选）
```

**实例 1：捕获特定异常**



```python
try:
    num = int(input("请输入数字："))
    print(10 / num)
except ValueError:
    print("输入错误：请输入整数！")
except ZeroDivisionError:
    print("计算错误：除数不能为0！")
```

**运行示例**：



```plain&#x20;text
请输入数字：abc
输入错误：请输入整数！
```

**实例 2：`else` 和 `finally` 子句**



```python
try:
    f = open("data.txt", "r")
except FileNotFoundError:
    print("文件不存在！")
else:# 无异常时读取文件
    print("文件内容：", f.readline())
    f.close()
finally:# 无论是否异常，都会执行
    print("操作结束")
```

* 抛出异常（`raise` 语句）

主动触发异常，用于自定义错误检查。

**语法**：



```python
raise 异常类型(错误信息)
```

**实例**：



```python
def check_age(age):
    if age < 0:# 主动抛出 ValueError
        raise ValueError("年龄不能为负数！")
        print(f"年龄为：{age}")
        try:
            check_age(-5)
        except ValueError as e:
            print("错误：", e)  # 输出：错误：年龄不能为负数！
```

* 用户自定义异常

通过继承 `Exception` 类创建自定义异常，用于特定业务场景。

**实例**：



```python
# 自定义异常类
class ScoreError(Exception):
    def __init__(self, score):
        self.score = score
        self.message = f"分数 {score} 无效（必须在0-100之间）"
    def check_score(score):
        if not (0 <= score <= 100):
            raise ScoreError(score)  # 抛出自定义异常
        try:
            check_score(150)
        except ScoreError as e:
            print(e.message)  # 输出：分数 150 无效（必须在0-100之间）
```

* 断言（`assert`）

`assert` 用于调试阶段验证条件，条件为 `False` 时触发 `AssertionError`，可附带错误信息。

**语法**：



```python
assert 条件, 错误信息  # 条件为False时触发异常
```

**实例**：



```python
def calculate(a, b):# 确保b不为0（调试用）
    assert b != 0, "除数b不能为0！"
    return a / b

calculate(10, 0)  # 触发 AssertionError: 除数b不能为0！
```

> **注意**：断言可通过 `-O` 选项关闭（生产环境不生效），不宜替代正常异常处理。
>
> ##### 总结

* **语法错误**：编写代码时避免，解释器会直接提示；

* **异常处理**：用 `try-except` 捕获并处理运行时错误，保证程序稳定性；

* **主动抛异常**：通过 `raise` 和自定义异常类，实现业务规则校验；

* **断言**：用于调试阶段验证条件，不建议在生产环境依赖。

合理处理异常是编写健壮 Python 程序的关键，可有效提升代码可靠性和可维护性。

#### Python3 面向对象

面向对象编程（OOP）通过类和对象组织代码，核心是封装、继承和多态。Python 支持完整的面向对象特性，语法简洁灵活。

1. 类与对象

* **类（Class）**：定义对象的属性（数据）和方法（行为）的模板。

* **对象（Object）**：类的实例，具体的实体。

###### 定义类与创建对象



```python
# 定义类
class Person:# 类变量（所有实例共享）
    species = "人类"# 构造方法（初始化对象）
    def __init__(self, name, age):# 实例变量（每个实例独有）
        self.name = name
        self.age = age
    
    # 实例方法
    def greet(self):
        print(f"你好，我叫{self.name}，今年{self.age}岁")# 创建对象（实例化）
p1 = Person("张三", 20)
p2 = Person("李四", 25)# 访问属性和方法
print(p1.name)       # 输出：张三
p2.greet()           # 输出：你好，我叫李四，今年25岁
print(Person.species) # 输出：人类（访问类变量）
```

* `init` 是构造方法，实例化时自动调用，用于初始化属性；

* `self` 代表实例本身，必须作为方法的第一个参数（名称可自定义，但约定用 `self`）。

- 继承

子类继承父类的属性和方法，可扩展或重写父类功能。

###### 单继承



```python
# 父类
class Animal:
    def __init__(self, name):
        self.name = name
    
    def speak(self):
        print("动物发出声音")# 子类（继承 Animal）
class Dog(Animal):# 重写父类方法
    def speak(self):
        print(f"{self.name}汪汪叫")# 实例化子类
dog = Dog("旺财")
dog.speak()  # 输出：旺财汪汪叫（调用重写的方法）
```

###### 多继承

一个类可继承多个父类（按顺序搜索方法）：



```python
class A:
    def method(self):
        print("A的方法")
class B:
    def method(self):
        print("B的方法")# 继承 A 和 B
class C(A, B):
    pass

c = C()
c.method()  # 输出：A的方法（优先调用左侧父类的方法）
```

* 方法重写与 `super()`

子类可重写父类方法，通过 `super()` 调用父类版本。



```python
class Parent:
    def func(self):
        print("父类方法")
class Child(Parent):
    def func(self):# 调用父类方法
        super().func()
        print("子类方法")

child = Child()
child.func()# 输出：# 父类方法# 子类方法
```

* 访问控制（私有属性与方法）

- 以 **两个下划线 `__`** 开头的属性 / 方法为私有，类外部无法直接访问（实际是名称修饰）。

- 以 **一个下划线 `_`** 开头的为受保护属性，约定不对外公开。



```python
class Student:def __init__(self, name, score):
        self.name = name
        self.__score = score  # 私有属性# 私有方法
        def __show_score(self):
            print(f"分数：{self.__score}")# 公开方法访问私有成员
        def get_grade(self):
            self.__show_score()
            if self.__score >= 90:
                return "优秀"
            else:
                return "良好"

s = Student("王五", 85)
print(s.name)          # 输出：王五# print(s.__score)      # 报错：无法直接访问私有属性# s.__show_score()      # 报错：无法直接调用私有方法print(s.get_grade())   # 输出：分数：85 → 良好（通过公开方法访问）
```

* 类的特殊方法（运算符重载）

通过重写特殊方法（如 `add`、`str`）实现运算符重载或自定义行为。



```python
class Vector:def __init__(self, x, y):
        self.x = x
        self.y = y
    
    # 重载加法运算符
    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)# 重载字符串转换
    def __str__(self):
        return f"Vector({self.x}, {self.y})"

v1 = Vector(2, 3)
v2 = Vector(4, 5)
v3 = v1 + v2  # 调用 __add__ 方法
print(v3)     # 输出：Vector(6, 8)（调用 __str__ 方法）
```

* 类属性与实例属性

- **类属性**：定义在类中，所有实例共享，通过 `类名.属性` 访问。

- **实例属性**：定义在 `init` 中，每个实例独有，通过 `self.属性` 访问。



```python
class Car:# 类属性
    wheels = 4  # 所有车都有4个轮子
    def __init__(self, color):# 实例属性
        self.color = color  # 每辆车颜色可能不同

car1 = Car("红色")
car2 = Car("蓝色")
print(car1.wheels)  # 输出：4（访问类属性）
print(car2.color)   # 输出：蓝色（访问实例属性）
```

> ##### 总结

* 面向对象编程通过类封装数据和行为，提高代码复用性和可维护性；

* 继承允许子类扩展父类功能，多态通过方法重写实现不同对象的统一接口；

* 私有成员保护内部实现，特殊方法可自定义对象行为（如运算符重载）。

掌握面向对象编程是开发复杂 Python 应用的基础，尤其适合大型项目的模块化设计。

#### Python3 装饰器

装饰器（decorators）是 Python 中用于**动态修改函数或类行为**的高级特性，本质是一个接收函数 / 类并返回新函数 / 类的可调用对象。通过 `@装饰器名` 语法应用，可在不修改原代码的前提下扩展功能。

1. 装饰器基本用法

###### 函数装饰器

装饰器函数接收原函数作为参数，返回一个包装函数（`wrapper`），在包装函数中添加额外逻辑（如日志、计时等）。

**实例 1：简单装饰器（打印函数调用日志）**



```python
def log_decorator(func):
    def wrapper():
        print(f"准备调用函数：{func.__name__}")
        func()  # 调用原函数
        print(f"函数 {func.__name__} 调用完成")
    return wrapper

# 应用装饰器@log_decorator
def greet():
    print("Hello, 装饰器！")

greet()# 输出：# 准备调用函数：greet# Hello, 装饰器！# 函数 greet 调用完成
```

###### 带参数的原函数

通过 `*args` 和 `**kwargs` 让装饰器支持任意参数的原函数：

**实例 2：装饰带参数的函数**



```python
def time_decorator(func):import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)  # 传递参数并接收返回值
        end = time.time()
        print(f"{func.__name__} 耗时：{end - start:.2f}秒")
        return result  # 返回原函数结果
    return wrapper

@time_decorator
def calculate_sum(a, b):
    return a + b

print(calculate_sum(100000, 200000))# 输出：# calculate_sum 耗时：0.00秒# 300000
```

* 带参数的装饰器

装饰器本身可接收参数，需额外嵌套一层函数（装饰器工厂）。

**实例 3：控制函数调用次数的装饰器**



```python
def repeat(times):# 装饰器工厂：接收参数，返回装饰器
    def decorator(func):
        def wrapper(*args, **kwargs):
            for _ in range(times):
                func(*args, **kwargs)
        return wrapper
    return decorator

# 应用带参数的装饰器@repeat(3)  # 调用3次
def say_hi(name):
    print(f"Hi, {name}!")

say_hi("Python")# 输出：# Hi, Python!# Hi, Python!# Hi, Python!
```

* 类装饰器

类也可作为装饰器，需实现 `call` 方法（使类实例可调用），常用于更复杂的逻辑（如单例模式、状态管理）。

**实例 4：单例模式装饰器（确保类仅实例化一次）**



```python
class Singleton:def __init__(self, cls):
        self.cls = cls
        self.instance = None  # 存储唯一实例
        def __call__(self, *args, **kwargs):
            if self.instance is None:
            self.instance = self.cls(*args, **kwargs)
        return self.instance

# 应用类装饰器@Singleton
class Config:
    def __init__(self):
        print("Config 实例初始化")# 多次实例化，实际返回同一个对象
c1 = Config()
c2 = Config()print(c1 is c2)  # 输出：True（证明是同一个实例）
```

* 内置装饰器

Python 提供多个内置装饰器，简化类方法定义：

| 装饰器           | 作用                   | 实例                   |
| ------------- | -------------------- | -------------------- |
| @staticmethod | 定义静态方法（无 self 或 cls） | 无需实例化，直接用 类名.方法() 调用 |
| @classmethod  | 定义类方法（第一个参数为 cls）    | 访问类属性，用 类名.方法() 调用   |
| @property     | 将方法转为属性（可像属性一样访问）    | 用于封装 getter/setter   |

**实例 5：内置装饰器用法**



```python
class Circle:
    pi = 3.14159  # 类属性
    def __init__(self, radius):
        self._radius = radius

    @staticmethoddef info():
        print("这是一个圆形类")
    @classmethod
    def calculate_area_by_diameter(cls, diameter):
        radius = diameter / 2
        return cls.pi * radius**2
    @property
    def radius(self):
        return self._radius  # getter@radius.setter
        def radius(self, value):
            if value > 0:
                self._radius = value  # setter
            else:
                raise ValueError("半径必须为正数")# 静态方法
Circle.info()  # 输出：这是一个圆形类# 类方法
print(Circle.calculate_area_by_diameter(10))  # 输出：78.53975# 属性装饰器
c = Circle(5)
print(c.radius)  # 输出：5（调用 getter）
c.radius = 6     # 调用 setter
print(c.radius)  # 输出：6
```

* 多个装饰器堆叠

多个装饰器可按顺序应用于同一函数，执行顺序为**从下到上**（先装饰的后执行）。

**实例 6：装饰器堆叠**



```python
def decorator_a(func):
    def wrapper():
        print("装饰器A：前")
        func()
        print("装饰器A：后")
    return wrapper

def decorator_b(func):
    def wrapper():
        print("装饰器B：前")
        func()
        print("装饰器B：后")
     return wrapper

# 堆叠装饰器（先应用 decorator_b，再应用 decorator_a）
@decorator_a@decorator_b
def test():
    print("原函数执行")

test()# 输出：# 装饰器A：前# 装饰器B：前# 原函数执行# 装饰器B：后# 装饰器A：后
```

> ##### 装饰器的应用场景

* **日志记录**：自动记录函数调用参数、返回值和时间；

* **性能分析**：测量函数执行时间；

* **权限验证**：调用函数前检查用户权限；

* **缓存**：缓存函数结果，避免重复计算；

* **输入验证**：检查函数参数是否符合要求。

装饰器是 Python 代码复用和功能扩展的强大工具，合理使用可显著提升代码的简洁性和可维护性。
