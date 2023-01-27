# 概述

用于列出指定路径下的文件（Linux中一切皆文件，目录也是文件的一种），如果不指定路径，单独运行ls命令，则默认路径为当前路径

# 语法
ls [-options] [target path]

# 常见参数

- -a：列出目标目录下所有文件，包含隐藏文件
- -l：显示文件的详细信息，包括文件类型，权限，所属用户，所属用户组，文件大小，上一次修改时间等
- -h：文件大小以KBytes为单位显示
- -S：按照文件大小顺序显示，默认从大到小；若要从小到大，可使用-Sr

# 案例
1、列出当前目录下所有文件
```
$ ls -a
.      book.json     Gitbook  Kafka详解  node_modules  SUMMARY.md  数据库
..     Cloud Native  Golang   logs       README.md     操作系统
_book  .git          images   Nginx详解  SRE           日志管理
```
2、列出当前目录下所有文件的详细信息
```
$ ls -al
总用量 88
drwxr-xr-x   16 root root  4096 12月 23 20:47 .
dr-xr-x---.  13 root root  4096 12月 23 20:40 ..
drwxr-xr-x   15 root root  4096 12月 23 20:40 _book
-rw-r--r--    1 root root  2852 12月 23 20:19 book.json
drwxr-xr-x    4 root root  4096 12月 23 17:36 Cloud Native
drwxr-xr-x    7 root root  4096 12月 23 18:18 .git
drwxr-xr-x    3 root root  4096 12月 23 20:21 Gitbook
drwxr-xr-x    2 root root  4096 12月 23 16:19 Golang
drwxr-xr-x    2 root root  4096 12月 23 20:24 images
drwxr-xr-x    3 root root  4096 12月 23 16:12 Kafka详解
drwxr-xr-x    2 root root  4096 12月 23 18:16 logs
drwxr-xr-x    4 root root  4096 12月 23 16:16 Nginx详解
drwxr-xr-x  199 root root 12288 12月 23 20:13 node_modules
-rw-r--r--    1 root root   164 12月 23 20:25 README.md
drwxr-xr-x    5 root root  4096 12月 23 18:00 SRE
-rw-r--r--    1 root root  4333 12月 23 20:40 SUMMARY.md
drwxr-xr-x    3 root root  4096 12月 23 20:35 操作系统
drwxr-xr-x    3 root root  4096 12月 23 18:36 日志管理
drwxr-xr-x    2 root root  4096 12月 23 17:40 数据库
```
3、列出当前目录下所有文件的详细信息，文件大小以KBytes为单位
```
$ ls -alh
总用量 88K
drwxr-xr-x   16 root root 4.0K 12月 23 20:47 .
dr-xr-x---.  13 root root 4.0K 12月 23 20:40 ..
drwxr-xr-x   15 root root 4.0K 12月 23 20:40 _book
-rw-r--r--    1 root root 2.8K 12月 23 20:19 book.json
drwxr-xr-x    4 root root 4.0K 12月 23 17:36 Cloud Native
drwxr-xr-x    7 root root 4.0K 12月 23 18:18 .git
drwxr-xr-x    3 root root 4.0K 12月 23 20:21 Gitbook
drwxr-xr-x    2 root root 4.0K 12月 23 16:19 Golang
drwxr-xr-x    2 root root 4.0K 12月 23 20:24 images
drwxr-xr-x    3 root root 4.0K 12月 23 16:12 Kafka详解
drwxr-xr-x    2 root root 4.0K 12月 23 18:16 logs
drwxr-xr-x    4 root root 4.0K 12月 23 16:16 Nginx详解
drwxr-xr-x  199 root root  12K 12月 23 20:13 node_modules
-rw-r--r--    1 root root  164 12月 23 20:25 README.md
drwxr-xr-x    5 root root 4.0K 12月 23 18:00 SRE
-rw-r--r--    1 root root 4.3K 12月 23 20:40 SUMMARY.md
drwxr-xr-x    3 root root 4.0K 12月 23 20:35 操作系统
drwxr-xr-x    3 root root 4.0K 12月 23 18:36 日志管理
drwxr-xr-x    2 root root 4.0K 12月 23 17:40 数据库
```
4、列出根目录下所有文件的详细信息，文件大小以KBytes为单位
```
$ ls -alh /
总用量 76K
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:53 .
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:53 ..
lrwxrwxrwx.   1 root root    7 3月   7 2019 bin -> usr/bin
dr-xr-xr-x.   5 root root 4.0K 4月  15 2022 boot
drwxr-xr-x    2 root root 4.0K 11月  5 2019 data
drwxr-xr-x   19 root root 3.0K 12月 22 21:02 dev
drwxr-xr-x.  88 root root 4.0K 12月 23 10:13 etc
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 home
lrwxrwxrwx.   1 root root    7 3月   7 2019 lib -> usr/lib
lrwxrwxrwx.   1 root root    9 3月   7 2019 lib64 -> usr/lib64
drwx------.   2 root root  16K 3月   7 2019 lost+found
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 media
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 mnt
drwxr-xr-x.   3 root root 4.0K 3月   7 2019 opt
dr-xr-xr-x  108 root root    0 12月 22 21:02 proc
drwxr-xr-x    2 root root 4.0K 12月 22 23:10 quick-start
dr-xr-x---.  13 root root 4.0K 12月 23 20:40 root
drwxr-xr-x   28 root root  980 12月 23 10:13 run
lrwxrwxrwx.   1 root root    8 3月   7 2019 sbin -> usr/sbin
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 srv
dr-xr-xr-x   13 root root    0 12月 22 21:02 sys
drwxrwxrwt.  39 root root 4.0K 12月 23 20:47 tmp
drwxr-xr-x.  13 root root 4.0K 3月   7 2019 usr
drwxr-xr-x.  19 root root 4.0K 3月   7 2019 var
```
5、列出根目录下所有文件的详细信息，文件大小以KBytes为单位，并且按照文件大小进行排序
```
$ ls -alhS /
总用量 76K
drwx------.   2 root root  16K 3月   7 2019 lost+found
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:55 .
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:55 ..
dr-xr-xr-x.   5 root root 4.0K 4月  15 2022 boot
drwxr-xr-x    2 root root 4.0K 11月  5 2019 data
drwxr-xr-x.  88 root root 4.0K 12月 23 10:13 etc
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 home
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 media
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 mnt
drwxr-xr-x.   3 root root 4.0K 3月   7 2019 opt
drwxr-xr-x    2 root root 4.0K 12月 22 23:10 quick-start
dr-xr-x---.  13 root root 4.0K 12月 23 20:40 root
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 srv
drwxrwxrwt.  39 root root 4.0K 12月 23 20:47 tmp
drwxr-xr-x.  13 root root 4.0K 3月   7 2019 usr
drwxr-xr-x.  19 root root 4.0K 3月   7 2019 var
drwxr-xr-x   19 root root 3.0K 12月 22 21:02 dev
drwxr-xr-x   28 root root  980 12月 23 10:13 run
lrwxrwxrwx.   1 root root    9 3月   7 2019 lib64 -> usr/lib64
lrwxrwxrwx.   1 root root    8 3月   7 2019 sbin -> usr/sbin
lrwxrwxrwx.   1 root root    7 3月   7 2019 bin -> usr/bin
lrwxrwxrwx.   1 root root    7 3月   7 2019 lib -> usr/lib
dr-xr-xr-x  108 root root    0 12月 22 21:02 proc
dr-xr-xr-x   13 root root    0 12月 23 20:54 sys
```
6、列出根目录下所有文件的详细信息，文件大小以KBytes为单位，并且按照文件大小进行倒序显示
```
$ ls -alhSr /
总用量 76K
dr-xr-xr-x   13 root root    0 12月 23 20:54 sys
dr-xr-xr-x  107 root root    0 12月 22 21:02 proc
lrwxrwxrwx.   1 root root    7 3月   7 2019 lib -> usr/lib
lrwxrwxrwx.   1 root root    7 3月   7 2019 bin -> usr/bin
lrwxrwxrwx.   1 root root    8 3月   7 2019 sbin -> usr/sbin
lrwxrwxrwx.   1 root root    9 3月   7 2019 lib64 -> usr/lib64
drwxr-xr-x   28 root root  980 12月 23 10:13 run
drwxr-xr-x   19 root root 3.0K 12月 22 21:02 dev
drwxr-xr-x.  19 root root 4.0K 3月   7 2019 var
drwxr-xr-x.  13 root root 4.0K 3月   7 2019 usr
drwxrwxrwt.  39 root root 4.0K 12月 23 20:47 tmp
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 srv
dr-xr-x---.  13 root root 4.0K 12月 23 20:40 root
drwxr-xr-x    2 root root 4.0K 12月 22 23:10 quick-start
drwxr-xr-x.   3 root root 4.0K 3月   7 2019 opt
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 mnt
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 media
drwxr-xr-x.   2 root root 4.0K 4月  11 2018 home
drwxr-xr-x.  88 root root 4.0K 12月 23 10:13 etc
drwxr-xr-x    2 root root 4.0K 11月  5 2019 data
dr-xr-xr-x.   5 root root 4.0K 4月  15 2022 boot
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:56 ..
dr-xr-xr-x.  20 root root 4.0K 12月 23 20:56 .
drwx------.   2 root root  16K 3月   7 2019 lost+found
```
