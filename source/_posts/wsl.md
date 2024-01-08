---
title: WSL适用于Windos的linux子系统
---

# WSL

## 优点

1. 原生 Linux 环境：WSL 允许在 Windows 系统上运行原生的 Linux 发行版，如 Ubuntu、Debian 等。这意味着你可以在 Windows 上使用 Linux 的命令行工具和应用程序，而无需使用虚拟机或双启动系统。

2. 无缝集成：WSL 与 Windows 系统紧密集成，可以直接访问 Windows 文件系统中的文件。这意味着你可以在 WSL 中轻松地访问和操作 Windows 文件，以及在 Windows 和 Linux 之间共享文件。

3. 开发环境一致性：如果你是在 Linux 上进行开发的，使用 WSL 可以在 Windows 上获得与 Linux 相同的开发环境。这样可以避免在不同操作系统之间切换时出现的兼容性问题，并且可以更轻松地与其他 Linux 开发者进行协作。

4. 轻量级：相比于虚拟机，WSL 是一种轻量级的解决方案。它不需要额外的硬件资源，且启动和运行速度较快。

5. 易于安装和配置：WSL 是作为 Windows 10 的一部分提供的，因此安装和配置过程相对简单。只需在 Windows 设置中启用 WSL 功能，并从 Microsoft Store 中下载所需的 Linux 发行版即可。

6. wsl 仅仅是可以运行 linux 中的二进制文件,不能操作 linux 的内核,所以不能用于 openstack 的开发.

## 先决条件

必须运行 Windows 10 版本 2004 及更高版本（内部版本 19041 及更高版本）或 Windows 11 才能使用以下命令.

## 安装 WSL 命令

- 在 Windows 10 或者 Windows 11 中，使用管理员打开 Powershell，然后执行下面的命令就可以开启 WSL 并安装 Ubuntu 作为默认的 WSL 发行版
  `wsl --install `
  `wsl --update`

- 查询可用的发行版
  `wsl --list --online`

- 安装一个发行版
  `wsl --install -d <Distribution Name>`
  - 注意，默认安装 WSL 2。如果你很早以前就安装过 WSL 1，可以执行 `wsl --set-version <distro> 2`命令把默认版本替换为 2

## 主要命令

- 进入 wsl
  `wsl`
- 检查状态
  `wsl --status`

- 检查版本
  `wsl --version`

- 以特定的用户身份进入
  `wsl -u <Username>`, `wsl --user <Username>`

## 导入导出

`wsl --export <Distribution Name> <FileName>`
`wsl --import <Distribution Name> <InstallLocation> <FileName>`

- 将已安装的 Linux 发行版导出为 tar 文件，或者将 tar 文件导入为新的发行版。这两条命令常用的场景为：当某个项目需要根据使用说明手册的步骤在 Windwos 系统安装 Linux 子系统，并需要在 Linux 子系统中安装其他软件或配置功能时（比如 linux adb），如果其他人已经在自己的电脑中安装好了一切。那么可以让他把已安装的发行版导出为 tar 文件，我只需要把这个 tar 文件导入即可，实现一键 copy 对方的系统和环境

## 参考网址

[WSL 网址](https://learn.microsoft.com/zh-cn/windows/wsl/)
