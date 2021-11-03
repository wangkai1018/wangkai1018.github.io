---
title: python的pandas基础
tags:
  - python
  - 笔记
date: 2020-05-07 08:48:49
---
## python的pandas基础
江湖上流传着这么一句话——分析不识潘大师（PANDAS），纵是老手也枉然。Pandas是基于Numpy的专业数据分析工具，可以灵活高效的处理各种数据集，也是我们后期分析案例的神器。

### 基本概念
pandas提供了两种数据结构，分别是**DataFrame**和**Series**。所有的pandas的骚操作都是基于于此。

* DataFrame：可以简单的理解为Excel中的表格	
* Series：Series可以理解为表中的一列

### 表格的创建
构造DataFrame最简单的方式是字典+列表，也就是python的**Dictionary**+**List**。Dictionary是键值对集合数据类型，理解为存储表格中的列的数据；列名为**key**,**value**为该列的所有数据值；其中的value的数据类型就是**List**，存储该列值的具体明细。表格的创建既有列，还有横行，即**index**。熟悉这个之后，对于Excel的创建就有了一个初步的了解。如下：


	import pandas as pd 
	df1=pd.DataFrame({'工资':[9000,7000,4000,8000,100000],'绩效':[86,91,74,83,97],'性别':['男','女','女','女','女']},index=['王闵京','陈红英','张秀影','王春芳','陈春月'])
	print(df1)

运行后会出现以下表格：

|        | 工资  | 绩效  | 性别 |
|:----|:----:| ----:|----:|
|王闵京|9000|86|男|
|陈红英|7000|91|女|
|张秀影|4000|74|女|
|王春芳|8000|83|女|
|陈春月|100000|97|女|

其中工资、绩效、性别一栏为columns(列)；第一列的名字为index;中间的值为values

### Excel和Csv文件的读取

	#csv文件的读取.
	#engine是使用的分析引擎，读取csv文件一般指定python避免中文和编码造成的报错
	df2=pd.read_csv('测试文件.csv',engine='python')
	df2.head()
	#xls和xlsx文件的读取
	df3=pd.read_excel('测试文件.xls')
	df3.head()

### 文件的保存

	df2.to_csv('要保存的名字.csv')
	df3.to_excel('要保存的名字.xlsx')

### 认识数据

	#查看默认前5行数据
	df2.head()
	#查看默认末尾5行数据
	df2.tail()
	#查看指定行数数据
	df2.head(10)
	#查看个列数据的类型
	df2.info()
	#快速查看数据类型的关键统计指标；像平均数、中位数、标准差等等
	#该方法只针对数值类型的值，其中count指的是统计每一列中有多少空值
	df2.describe()


### 获取数据的行数和列数

	# 获取行数
	 df2.shape[0] 
	 # 获取行数
	 len(df2)
	 # 获取列数
	 df2.shape[1] 

### 数据的增删改查
* 增
* 删
* 改
* 查(选)

**增**：

增加一列，用df['新列名'] = 新列值的形式，在原数据基础上赋值即可

```
df2['新增的列名']=rang(1,len(df2)+1)
```
**删**：

axis = 1表示针对列的操作，inplace为True，则直接在源数据上进行修改，否则源数据会保持原样

```
#
df2.drop('删除的列',axis=1,inplace=True)
```
**改**：

df2['旧列名'] =  某个值或者某列值，就完成了对原列数值的修改


**查(选)**：

选取某一列：df2['列名']即可


### Excel文件的数据遍历

Pandas是python的数据分析包，提供了大量的快速便捷处理数据的函数和方法，其中遍历的方法有一下几种，处理效率从慢到快：

1. for in循环迭代方式
2. iterrows()生成器方式
3. apply()方法循环方式
4. Pandas series的矢量化方式
5. Numpy arrays的矢量化方式

总结

使用timeit方法对以上几种遍历方式进行执行时间测试，测试结果如下。可以看出循环执行的速度是最慢的，iterrows()针对Pandas的dataframe进行了优化，相比直接循环有显著提升。apply()方法也是在行之间进行循环，但由于利用了类似Cython的迭代器的一系列全局优化，其效率要比iterrows高很多。NumPy arrays的矢量化运行速度最快，其次是Pandas series矢量化。由于矢量化是同时作用于整个序列的，可以节省更多的时间，相比使用标量操作更好，NumPy使用预编译的C代码在底层进行优化，同时也避免了Pandas series操作过程中的很多开销，例如索引、数据类型等等，因此，NumPy arrays的操作要比Pandas series快得多。





---

本文笔记摘抄自[知乎吹牛Z](https://mp.weixin.qq.com/s?__biz=MzU5Mjg2OTQ1MA==&mid=2247484097&idx=1&sn=ad8fabbd84bf67655996026fc0ac5688&chksm=fe1863e4c96feaf200e9398bb7c824e99d3fc01ec965666497ce584466dc93f83dd5d127a46d&scene=21#wechat_redirect)
[CSDN「西山枫叶」](https://blog.csdn.net/wem603947175/article/details/84311873)