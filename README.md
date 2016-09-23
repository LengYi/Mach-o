
#Mach-o文件结构详解
下载测试 [Demo](git@github.com:LengYi/Mach-o.git) 使用Xcode编译成app，注意使用 product->archive 编译,然后导出app,
如果无法编译或者失败,请使用编译好的 MethodSwizzlingDemo。

Mach-o文件结构包含三个基本区域:

* 头部（header structure）。
+ 加载命令（load command）。
- 段（segment）。可以拥有多个段（segment），每个段可以拥有零个或多个区域（section）。每一个段（segment）都拥有一段虚拟地址映射到进程的地址空间。
* 链接信息。一个完整的用户级Mach-o文件的末端是链接信息。其中包含了动态加载器用来链接可执行文件或者依赖库所需使用的符号表，字符串表等等

![image](http://blog.chinaunix.net/uid/26495963.html)