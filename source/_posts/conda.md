---
title: Anaconda常用操作
---

#### 创建新环境

- 默认路径下
  `conda create --name <environment_name> python==<version>`

- 指定路径下创建环境
  `conda create --prefix=<路径> python==<version>`

#### 激活环境

1. 对于 windos 系统
   `conda activate <环境名称>`

2. 对于 Mac 和 Linux 系统
   `source activate <环境名称>`

#### 退出环境

1. 对于 windos 系统:
   `conda deactivate`

2. 对于 Mac 和 Linux 系统:
   `source deactivate`

#### 删除环境

- 要删除一个已经存在的 conda 环境，可以使用以下命令：
  `conda remove --name <环境名称> --all`

#### 复制环境

- 要复制一个已经存在的 conda 环境
  `conda create --name <新环境名称> --clone <源环境名称>`

#### 查看信息

| 命令                        |
| --------------------------- |
| `conda info`                |
| `conda -V`                  |
| `conda search package_name` |

#### vscode 中使用 conda 的虚拟环境

| 步骤 | 选择解析器                                      | 默认为 cmd                                        |
| ---- | ----------------------------------------------- | ------------------------------------------------- |
| 1    | 输入`ctrl+shift+p`出现命令提示符                | 输入`ctrl+shift+p`出现命令提示符                  |
| 2    | 然后输入`python select interpret`即可选择解析器 | 然后输入`select default prompt`即可设置默认提示符 |

#### 配置环境变量

| 路径                               |
| ---------------------------------- |
| `A:\software\Anaconda`             |
| `A:\software\Anaconda\Scripts`     |
| `A:\software\Anaconda\Library\bin` |

#### 修改默认缓存位置

1. 1 查看当前有哪些路径

```conda

#简单查询
conda info
#或者用这句能够直接看到 key：
conda config --show
```

1. 2 添加、删除 envs_dirs

```conda

#dir是路径
conda config --add envs_dirs dir
conda config --remove envs_dirs dir
#remove只能删除自己添加的路径，系统默认的就会报错
```

2. 第二种方法是进入 C:\Users\admin 修改.condarc 文件（默认隐藏的），末尾添加

```conda

envs directories :
  - D:\Anaconda3\envs
```
