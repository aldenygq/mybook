# 概述
Linux 系统文件检索工具，比grep好用

# 命令特点
- 默认搜索当前工作目录
- 默认递归搜索子目录
- 忽略元数据目录，比如.svn,.git,CSV等目录
- 忽略二进制文件（比如pdf，image，coredumps)和备份文件（比如foo~,*.swp)
- 在搜索结果中打印行号，有助于找到目标代码
- 能搜索特定文件类型（比如Perl,C++,Makefile),该文件类型可以有多种文件后缀
- 高亮搜索结果
- 支持Perl的高级正则表达式，比grep所使用GNU正则表达式更有表现力。

# 安装部署
```
$ wget http://beyondgrep.com/ack-2.12-single-file
$ sudo mv ack-2.12-single-file /usr/bin/ack
$ sudo chmod 0755 /usr/bin/ack
```
# 常用参数
- -n：显示行号
- -l/L：显示匹配/不匹配的文件名
- -c：统计次数
- -v：invert match
- -w：词匹配
- -i：忽略大小写
- -f：只显示文件名,不进行搜索.
- -h：不显示名称
- -v：显示不匹配

# 案例
1、在当前目录递归搜索单词”eat”,不匹配类似于”feature”或”eating”的字符串
```
$ ack -w eat
```
2、搜索有特殊字符的字符串’$path=.’,所有的元字符（比如’$’,’.’)需要在字面上被匹配
```
$ ack -Q '$path=.' /etc
```
3、除了dowloads目录，在所有目录搜索”about”单词
```
$ ack about --ignore-dir=downloads
```
4、只搜索包含’protected’单词的PHP文件，然后通过文件名把搜索结果整合在一起，打印每个文件对应的搜索结果
```
$ ack --php --group protected
```
5.获取包含’CFLAG’关键字的Makefile的文件名。文件名为.mk,makefile,Makefile,GNU makefile的都在考虑范围内 
```
$ ack --make -l CFLAG
```
6、显示整个日志文件时高亮匹配到的字符串
```
$ tail -f /var/log/syslog | ack --passthru 192.168.1.10
```
7、要换取ack支持的文件过滤类型
```
$ ack --help-type
```
