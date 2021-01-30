# <center>Makefile</center>

## makefile 规则
```
target ...: prerequisites ...
  command
...
...
```
`\`换行符

`.o`会自动将`.c`加入推导

`.PHONY : clean` 表示clean是一个伪目标

## 参数
`-f --file` 指定特定的文件进行make
`-I --include-dir` 指定include目录

## 总述
Makefile里主要包含了五个东西：显式规则、隐晦规则、变量定义、文件指示和注释。

>1. 显式规则。显式规则说明了，如何生成一个或多的的目标文件。这是由Makefile的书写者明显指出，要生成的文件，文件的依赖文件，生成的命令。
>2. 隐晦规则。由于我们的make有自动推导的功能，所以隐晦的规则可以让我们比较粗糙地简略地书写Makefile，这是由make所支持的。
>3. 变量的定义。在Makefile中我们要定义一系列的变量，变量一般都是字符串，这个有点你C语言中的宏，当Makefile被执行时，其中的变量都会被扩展到相应的引用位置上。
>4. 文件指示。其包括了三个部分，一个是在一个Makefile中引用另一个Makefile，就像C语言中的include一样；另一个是指根据某些情况指定Makefile中的有效部分，就像C语言中的预编译#if一样；还有就是定义一个多行的命令。有关这一部分的内容，我会在后续的部分中讲述。
>5. 注释。Makefile中只有行注释，和UNIX的Shell脚本一样，其注释是用“#”字符，这个就像C/C++中的“//”一样。如果你要在你的Makefile中使用“#”字符，可以用反斜框进行转义，如：“\#”。

## 引用其他makefile
`include <filename>`

## 规则中使用通配符
* "~"
  >波浪号(\~)字符在文件名中也有比较特殊的用途。如果是“~/test”，这就表示当前用户的$HOME目录下的test目录。而“~hchen/test”则表示用户hchen的宿主目录下的test目录。（这些都是Unix下的小知识了，make也支持）而在Windows或是MS-DOS下，用户没有宿主目录，那么波浪号所指的目录则根据环境变量“HOME”而定。
* "*"
  >通配符代替了你一系列的文件，如“\*.c”表示所以后缀为c的文件。一个需要我们注意的是，如果我们的文件名中有通配符，如：“\*”，那么可以用转义字符“\”，如“\*”来表示真实的“\*”字符，而不是任意长度的字符串。

## 文件搜寻
`VPATH = src : ../headers`
`vpath < pattern> < directories>` 为符合模式\<pattern\>的文件指定搜索目录\<directories\>
`vpath <pattern>` 清除符合模式\<pattern\>的文件的搜索目录。
`vpath` 清除所有已被设置好了的文件搜索目录。