---
title: mac终端工具描述
tags:
  - terminal
  - 笔记
date: 2020-04-17 17:09:07
---
## 已使用过的MAC终端工具
**nvm**：**nodejs**包管理工具，同时对多版本进行管理

**pyenv**:**python**多版本管理工具。可配合的镜像源为阿里,搜狐和豆瓣源不可用

**homebrew**: [homebrew](https://brew.sh/index_zh-cn.html)包管理工具，下载更新非常高效，全程终端进行，配合国内镜像使用速度很快。其中分为**cask**和**formula**模块。

* cask：为常用app模块,例如：优酷、爱奇艺
* formula:开发工具，开发环境的模块

**homebrew常用命令**：


	brew update         #更新homebrew
	brew upgrade [包名] #更新所有安装的软件包，也可单独指定更新
	brew search 包名    #查找软件包
	brew install 包名   #安装软件包
	brew list          #列出已安装的软件包
	brew uninstall 包名 #卸载软件包
	brew outdated      #列出可以更新的软件包
	brew info 包名      #查看软件包的信息
	brew cask list     #列出cask下已安装的软件包
	brew cask install 包名 #安装cask下的能安装的软件包
	brew cask outdated [包名] #列出可以更新的软件包,也可指定包名
	brew cask upgrade [包名] #更新所有的软件包，也可指定包名更新
	brew cleanup             # 清理所有包的旧版本
	brew cleanup $FORMULA    # 清理指定包的旧版本
	brew cleanup -n          # 查看可清理的旧版本包，不执行实际操作

**pip**:python的扩展包管理工具，mac、windows版本的python有的没有自带，需要手动下载安装。配合豆瓣镜像下载很快。

**conda**:conda是一个开源包管理系统和环境管理系统,跨平台。

**Anaconda**：Anaconda是一个开源的Python发行版本，包含了conda、python等180多个科学包及其依赖项。因为包含了大量的科学包，所以Anaconda的安装包比较大。如果为了省时间，也可以使用**Miniconda**这个较小的发行版。












