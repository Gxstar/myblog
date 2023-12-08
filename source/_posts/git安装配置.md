---
title: git安装配置
date: 2023-06-11 23:34:04
tags:
---

## Git配置指引（个人备份）

### 下载

>[git官网地址](https://git-scm.com/downloads)
>
>[清华镜像](https://mirrors.tuna.tsinghua.edu.cn/github-release/git-for-windows/git/)

### 安装

>狂点下一步就好

### 本地配置

> 1. 查看git版本：git version
> 2. 配置用户名：git config --global user.name "gxstar"
> 3. 配置邮箱：git config --global user.email “<gengxing123@qq.com>”
> 4. 查询配置：git config --global --list
> 5. 生成密钥文件：ssh-keygen -t rsa

### github配置

>- 密钥文件默认生成位置：C:\Users\gengx\.ssh\id_rsa.pub（如果在生成密钥时选择了更改了存储位置则在指定位置处）
>1. 登录github
>2. 右上角头像点击后选择Settings
>[![](https://pic.imgdb.cn/item/6485f2811ddac507cc4d2581.jpg)](https://pic.imgdb.cn/item/6485f2811ddac507cc4d2581.jpg)
>3. 点击设置密钥
>[![](https://pic.imgdb.cn/item/6485f2db1ddac507cc4d8787.jpg)](https://pic.imgdb.cn/item/6485f2db1ddac507cc4d8787.jpg)
>4. 新建密钥填入上面打开的id_rsa.pub的内容，标题自拟就行
>[![](https://pic.imgdb.cn/item/6485f33b1ddac507cc4df5b6.jpg)](https://pic.imgdb.cn/item/6485f33b1ddac507cc4df5b6.jpg)
>5. 重装git后避免无法直接重新使用项目：git config --global --add safe.directory "*";
>5. 配置完成