---
title: python常用命令
tags:
  - python
  - 笔记
date: 2020-04-27 12:43:58
---
## python常用包、工具、命令
**pip**：[pip](https://pypi.org/project/pip/)是常用的[python](https://www.python.org/)包管理工具，类似于**java**的**maven**。用python的同学，都离不开pip。在Python2.7的安装包中，**easy_install.py**是默认安装的，而pip需要我们手动在终端中进行安装：

`sudo easy_install pip`

### pip的常用命令

```
pip --version #查看版本
pip list #已安装包库列表
pip install 包名 #安装指定的包库
pip install --upgrade 库名 #更新指定的包库
pip list --outdated  #查看过期的库(需要更新的库)
pip uninstall 包名 #卸载已安装包
```
### mac pip更换豆瓣镜像源
1. 在mac终端创建目录`md ~/.pip`
2. 并在目录中创建文件`vim ~/.pip/pip.conf`
3. 并在该文件中录入以下内容：

```
[global]
  index-url = https://pypi.tuna.tsinghua.edu.cn/simple/
[install]
  trusted-host=pypi.tuna.tsinghua.edu.cn
```

### windows pip更换豆瓣镜像源
1. 在windows文件管理器中,输入 `%APPDATA%`
2. 定位到上述目录下，新建**pip**文件夹，然后在该文件中新建一个**pip.ini**文件
3. 在新建的**pip.ini**文件中录入以下内容：

```
[global]
timeout = 6000
index-url = http://pypi.douban.com/simple
trusted-host = pypi.douban.com
```

### 终端运行python文件
`python test.py arg1 arg2 arg3
`
### conda的使用
```
conda --version  #当前使用版本	
conda list  #查看当前环境下已安装的包
conda search 包名  #查找package信息
conda install 包名   #安装库
conda update 包名  #更新单一库
conda update -all   #更新所有的库          
conda update conda #更新conda

```

### python的路径
Mac下的python的各种路径：

* 自带路径：mac自带的版本为2.7。路径为:/System/Library/Frameworks/Python.framework/Version
* brew安装路径：HomeBrew安装python路径为/usr/local/Cellar/python里边存放了HomeBrew所安装版本。

