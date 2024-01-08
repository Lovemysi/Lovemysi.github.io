---
title: SSH 连接远程服务器
---

### Windos Terminal :SSH 连接远程服务器

- Windos terminal 是新一代 Windos 终端,支持使用密钥，实现免密码登录

- win + R 运行 wt

#### 1.使用密码登录

```sh
ssh user@host
#例如: root@192.168.136.114
```

#### 2.使用密钥登录

-- 密钥登录时，首先需要生成公钥和私钥

1. **登录**

```sh
$ ssh-keygen
#回车就行了
```

```sh
cat ~/.ssh/id_rsa.pub | ssh user@host "mkdir -p ~/.ssh && cat >> ~/.ssh/authorized_keys"
#user@host 处需要修改
##例: root@192.168.136.114
```

```sh
ssh user@host
#例如: root@192.168.136.114
```

2.  **快捷登录**

```sh
#导航栏下拉进入设置-配置文件-添加新配置文件-新建空配置文件。在命令行一栏填入：
ssh user@ip
#或 ssh -i 密钥路径 user@ip
##例:ssh -i C:\Users\星辰\.ssh/id_rsa root@192.168.31.78
```
