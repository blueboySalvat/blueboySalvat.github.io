##### 问题一：DOS 与 windows 中 cmd 区别

在windows系统中，“开始-运行-cmd”可以打开“cmd.exe”，进行命令行操作。 操作系统可以分成核心（kernel）和Shell（外壳）两部分，其中，Shell是操作系统与外部的主要接口，位于操作系统的外层，为用户提供与操作系统核心沟通的途径。在windows系统中见到的桌面即explorer.exe（资源管理器）是图形shell，而cmd就是命令行shell。这算是cmd与dos的最大区别，一个**只是接口**、一个是操作系统。只是cmd中的某些命令和dos中的命令相似，因此很多人把二者混为一谈。cmd属于windows系统的一部分，dos本身就是一个系统，在dos系统下可以删除，修复windows系统，而在cmd下则不行。

##### 问题二：Linux下的shell是什么？

Shell俗称壳（用来区别于核 kernel），是一种“命令解析器”。按照ABS的定义，shell是The shell is a command interpreter. More than just the insulating layer between the operating system kernel and the user, it’s also a fairly powerful programming language。分为图形界面shell和命令行shell两大类。 Shell管理你与操作系统之间的交互：等待你输入，向操作系统解释你的输入，并且处理各种各样的操作系统的输出结果。不同系统有不同的shell，如bash、C shell、windows power shell 等等；在linux系统中，通常是Bourne Again shell ( 即bash)。

##### 问题三：windows下能用bash shell吗？

bash是Linux和Unix下的shell，如果真的想试用，可以在MS windows下安装Cygwin环境，然后再在其下使用。 这时需要注意，Cygwin环境下跟真实的Linux或Unix是有区别的，一些命令会运行不正常。最直接的体验，还是使用Linux来得贴心，几乎可以做任何事情。如果想在MS Windows下使用Shell，建议还是使用微软的PowerShell，它能提供给你操作MS windows的完全功能。

##### 问题四：脚本语言和普通的编程语言有什么区别？

编程语言 “编写-编译-链接-运行”，脚本语言是“解释-执行”而非编译，脚本语言的程序代码即使最终的可执行文件，通过对应的解释器解释执行即可，所以更方便快捷。每种脚本语言都需要其对应的解释器。如Perl、Python、Ruby、JavaScript等都是脚本语言，shell也属于一种比较特殊的脚本语言。

##### 问题五：linux shell即bash和windows cmd区别？

shell 是一个命令解释器(也是一种应用程序)，处于内核和用户之间，负责把用户的指令传递给内核并且把执行结果回显给用户，同时，shell 也可以作为一门强大的编程语言。在 linux/unix 平台上，shell 多半默认为 Bash shell。 cmd 是 Command shell 的简写，微软的定义是：The command shell is a separate software program that provides direct communication between the user and the operating system. The non-graphical command shell user interface provides the environment in which you run character-based applications and utilities. The command shell executes programs and displays their output on the screen by using individual characters similar to the MS-DOS command interpreter [Command.com](https://cloud.tencent.com/developer/tools/blog-entry?target=http%3A%2F%2Fcommand.com%2F&source=article&objectId=1477119).（CommandShell 是一个独立的应用程序，它为用户提供对操作系统直接通信的功能，它为基于字符的应用程序和工具提供了非图形界面的运行环境，它执行命令并在屏幕上回显 MS-DOS 风格的字符。）所以，可以近似地认为 linux shell=bash 而 windows=cmd，都是命令行解释器，都是用户与操作系统的交互接口。但是 bash 要比 cmd 强大很多，windows 也有强大的 shell 叫 windows power shell。


参考链接
[shell、cmd、dos和脚本语言区别和联系 - 闻道又又鱼 - 博客园](https://www.cnblogs.com/steamedfish/p/7123749.html)