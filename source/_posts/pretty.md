---
title: 操作系统
---

## 操作系统

#### windos 和 linux(xshell)之间的文件传输

|          | 执行命令                                                                 |
| -------- | ------------------------------------------------------------------------ |
| apt 命令 | [apt 命令使用链接](https://baike.baidu.com/item/apt/20109246?fr=aladdin) |
| 安装     | apt-get install lrzsz                                                    |
| 输入命令 | rz                                                                       |
| 小插入   | https://anzhiy.cn/posts/ddae.html                                        |

#### gcc 编译

预处理 编译 汇编 链接

```sh
-o 将操作的结果输入到指定文件中
直接将目标文件生成可执行文件: gcc  -o  生成文件  目标(*.c)文件
gcc 依赖文件 -o 目标文件
gcc -c hello.c
gcc -c 指令在添加一个 -o 选项，用于将汇编操作的结果输入到指定文件中
gcc -c hello.c -o test
链接生成可执行文件: gcc *.o -lpthread

```
