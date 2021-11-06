---
title: NVM的使用
tags:
  - NodeJS
  - 笔记
  - NVM
date: 2020-04-30 17:56:12
---
## NVM的使用

**NodeJS**的多版本管理系统,可以同一个机器上安装多个版本的环境，可以随时进行切换。版本管理mac还可以选择n；但是不支持windows。以下操作基于Mac：

	nvm ls-remote：     列出所有可以安装的node版本号
	nvm install v10.4.0：安装指定版本号的node
	nvm use v10.3.0：   切换node的版本，这个是全局的
	nvm current：        当前node版本
	nvm ls：                列出所有已经安装的node版本
	nvm uninstall          删除已安装的指定版本，语法与install类似
	nvm alias <name> <version>  给不同的版本号添加别名
	nvm unalias <name>          删除已定义的别名
	nvm reinstall-packages 在当前版本node环境下，重新全局安装指定版本号的npm包
	nvm list available    查看可以安装的版本
	nvm install stable    下载、编译、安装、使用当前的稳定版
	
	
**安装**

* curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
* 或者用homebrew 直接搜索nvm，进行安装

摘抄自[简书椰果粒](https://www.jianshu.com/p/0ffa636a6fe1)、[简书Wo信你个鬼](https://www.jianshu.com/p/7a33f2c19fea)


**国内源镜像**

由于网络原因,NVM在更新和下载时会很慢。可以设置国内的镜像源进行安装更新；速度很快，步骤如下：

1.  在终端中打开`vim ~/.zshrc`
2. 在配置文件中增加`export NVM_NODEJS_ORG_MIRROR=http://npm.taobao.org/mirrors/node`
3. 重启终端`source ~/.zshrc`；或者重开终端
4. 检查配置文件是否生效`echo $NVM_NODEJS_ORG_MIRROR`
 

如果最后输出http://npm.taobao.org/mirrors/node表明已经生效

-
> 本文摘抄自[简书omicron](https://www.jianshu.com/p/bc56e70303f7)


  
 






	
	

