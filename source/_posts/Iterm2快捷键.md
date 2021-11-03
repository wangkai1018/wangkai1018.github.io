---
title: Iterm2快捷键
tags:
  - Iterm2
  - 终端
date: 2020-05-25 14:21:48
---
## Iterm2快捷键

### 标签

	新建标签：command + t
	
	关闭标签：command + w
	
	改变标签的顺序：⌘ + shift + arrow
	
	切换标签：command + 数字 command + 左右方向键
	
	切换全屏：command + enter
	
	查找：command + f

### 分屏
	
	垂直分屏：command + d
	
	水平分屏：command + shift + d
	
	切换屏幕：command + option + 方向键 command + [ 或 command + ]
	
	查看历史命令：command + ;
	
	查看剪贴板历史：command + shift + h
	 
### 其他

	打开最近目录： ⌘ + alt + /

	清除当前行：ctrl + u
	
	到行首：ctrl + a
	
	到行尾：ctrl + e
	
	前进后退：ctrl + f/b (相当于左右方向键)
	
	上一条命令：ctrl + p
	
	搜索命令历史：ctrl + r
	
	删除当前光标的字符：ctrl + d
	
	删除光标之前的字符：ctrl + h
	
	删除光标之前的单词：ctrl + w
	
	删除到文本末尾：ctrl + k
	
	交换光标处文本：ctrl + t
	
	清屏1：command + r
	
	清屏2：ctrl + l
	
	自带有哪些很实用的功能/快捷键
	
	⌘ + 数字在各 tab 标签直接来回切换
	
	选择即复制 + 鼠标中键粘贴，这个很实用
	
	⌘ + f 所查找的内容会被自动复制
	
	⌘ + d 横着分屏 / ⌘ + shift + d 竖着分屏
	
	⌘ + r = clear，而且只是换到新一屏，不会想 clear 一样创建一个空屏
	
	ctrl + u 清空当前行，无论光标在什么位置
	
	输入开头命令后 按 ⌘ + ; 会自动列出输入过的命令
	
	⌘ + shift + h 会列出剪切板历史
	
	可以在 Preferences > keys 设置全局快捷键调出 iterm，这个也可以用过 Alfred 实现
 
### 即使回放
某个交互命令会覆写屏幕上的输入，之前的历史信息可能会被覆盖掉，无法查看，iterm2 这个及时回放功能，会记录历史输入，输出，有点类似视频录制。

	进入回放：⌘ + opt + b 
	
	方向键控制时间 ：arrow  
	
	退出回放：esc
 
###  标记条状

类似编辑器的mark工具，iTerm2也可以在命令行位置设置标记



	快速定位到光标所在位置： ⌘ + / 
 	
	设置标记：⌘ + shift + m
	
	跳转到上个标记：⌘ + shift + j
	
	多个标记切换：⌘ + shift + arrow
 
 
###  智能选中

双击选中，三击只能选中，四级智能选中

按住**command⌘**键：

1. 可以拖拽选中的字符串
2. 点击url：调用默认浏览器访问该网址
3. 点击文件：调用默认程序打开文件
4. .如果文件名是filename:42，且默认文本编辑器是 Mac vim将会直接打开到这一行；
5. 点击文件夹：在finder中打开该文件夹
6. 同时安装**option⌥**键，可以矩形选中
 
-
> 摘抄自[简书petter102](https://www.jianshu.com/p/50245a6e1f12)
> [简书ccrsky](https://www.jianshu.com/p/3436bcb17a03)

