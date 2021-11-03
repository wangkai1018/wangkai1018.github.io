---
title: NPM的使用
tags:
  - 笔记
  - NodeJS
  - NPM
date: 2020-05-21 13:27:35
---
## NPM的使用

### NodeJS基本命令

    console.log("Hello World");   #脚本模式
    node helloworld.js      #保存该文件，文件名为 helloworld.js， 并通过 node命令来执行
    node -v                 #查看node版本
    

### NPM的使用

**npm**是随同***NodeJS***一起安装的包管理工具，能解决NodeJS代码部署的很多问题，常见的使用场景有以下几种：

* 允许用户从npm服务器下载别人编写的第三方包到本地使用
* 允许用户从npm服务器下载并安装别人编写的命令行程序到本地使用
* 允许用户自己将自己编写的包或命令行程序上传到npm服务器供别人使用

#### npm的基本命令

	npm -v                     #查看版本
	sudo npm install npm -g    #升级npm版本
	npm install npm -g         #windows版本的升级命令
	npm install -g cnpm --registry=https://registry.npm.taobao.org    #使用淘宝镜像源升级
	npm install <Module Name>    #安装指定模块
	npm install express          # 本地安装
	npm install express -g     # 全局安装
	npm list -g                #查看全局安装的模块
	npm list  <-g> <Module Name>       #查看指定(本地或全局)模块的版本号
	npm unistall <Module Name>  #卸载指定的模块
	npm search <Module Name>    #搜索指定模块
	npm update <Module Name>   #更新全部或指定模块
	npm help   #查看帮助文档
	npm cache clear  #可以清空NPM本地缓存，用于对付使用相同版本号发布新版本代码的人
	npm unpublish <Module Name>@<version>   #可以撤销发布自己发布过的某个版本代码
      sudo npm cache clean -f   #清除node的cache（清除node的缓存，这个看情况而定，不是必须的）
	
#### npm镜像源管理

* npm修改配置文件
	* 步骤如下：
	    1. 查看*npm*源地址：`npm config list`   
	    2. 修改registry地址，比如修改为淘宝镜像源：  `npm set registry https://registry.npm.taobao.org/`
	    3. 如果不想用了，想删除：`npm config rm registry`
- 使用定制淘宝定制***cnpm***代替***npm***
    * 步骤如下：
        1. 全局安装cnpm： 
            * `npm install -g cnpm --registry=https://registry.npm.taobao.org`
        2. 成功后就可以用cnpm安装模块：
            * `cnpm install [Module Name] `
* 使用***nrm***专门进行管理和快速切换私人配置的registry,建议全局安装：
    1. 全局安装：
        * `npm install nrm -g --save`
    2. 常用命令：
        * 查看默认镜像源配置列表：
            * `nrm ls`
        * 输入以下命令查看当前使用的是哪个源
            * `nrm current`
        * 切换源：
            * `nrm use cnpm`
        * 添加私有npm源，并设置别名为qihoo，网址为自定义
	        *   `nrm add qihoo http://registry.npm.360.org`
        * 测试下速度
	        * `nrm test npm`  
        * 删除npm的源配置
	        * `nrm del qihoo`
        
#### 创建自己的模块

这个属于进阶内容，有自己想弄的模块在说吧

-
> 本文摘抄自[菜鸟教程](https://www.runoob.com/nodejs/nodejs-npm.html)
> [简书四月天__](https://www.jianshu.com/p/66f97cadd1eb)

	
 	

    
     
    
    

