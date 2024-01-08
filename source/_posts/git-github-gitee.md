---
title: git-github-gitee
---

### 图解 git

- 基础命令
  ![命令图鉴](https://pic.voiblog.top/others/2023/10/20/65327fe3359fb_2.png)

- 工作原理一览
  ![工作原理](https://pic.voiblog.top/others/2023/10/20/65327fec0f5c6_2.png)

### 密钥 SSH

| 类型        | 命令                                                            | 检查命令                |
| ----------- | --------------------------------------------------------------- | ----------------------- |
| gitee 密钥  | `ssh-keygen -t rsa -f ~/.ssh/id_rsa.gitee -C <"你的邮箱地址">`  | `ssh -T git@gitee.com`  |
| github 密钥 | `ssh-keygen -t rsa -f ~/.ssh/id_rsa.github -C <"你的邮箱地址">` | `ssh -T git@github.com` |

> 密钥: 利用密钥将本地仓库和远程仓库连接,实现免密登录
