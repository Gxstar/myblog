---
title: 编译最新版本的libraw到rawpy里
date: 2025-10-27 10:54:00
tags:
  - 编译
  - libraw
  - rawpy
  - Windows
---

## 环境说明

**编译基础环境：** Windows 11

## 编译最新版本 LibRaw

### 前置条件

- 安装好 Git
- 安装好 CMake
- 安装好 Visual Studio
- **重要：** 不能使用普通的 CMD 或 PowerShell，需要使用 "Developer Command Prompt for VS 2022"

### 编译步骤

```bash
git clone https://github.com/LibRaw/LibRaw.git
cd LibRaw
nmake -f Makefile.msvc
```

**编译结果会放在：** `LibRaw\Lib` 目录下

## 编译 rawpy

### 设置环境变量

```powershell
$env:USE_CONDA = '0'
$env:PYTHON_VERSION = '3.13'
$env:PYTHON_ARCH = 'x86_64'
$env:NUMPY_VERSION = '2.3.*'
```

### 编译步骤

```bash
git clone https://github.com/letmaik/rawpy
```

**文件替换操作：**
- 将前面编译好后的整个 LibRaw 目录复制替换到 rawpy 同名目录下
- LibRaw-cmake 放在 external 同名目录下

```bash
cd rawpy
.github/scripts/build-windows.ps1
```

**最终编译成果会放在：** `rawpy\dist` 目录下