---
layout: post
title: for循环的使用
categories: python
tags: for
---

* content
{:toc}

## for循环的使用

```python
>>> str="hello"
>>> for i in str:
...     print i
...
h
e
l
l
o
# 如果要打印为一行，加个","(英文逗号)即可
>>> for i in str:
...     print i,
...
h e l l o

# 如果要使用","号分割，可以使用"+"来实现
>>> for i in str:
...     print i+",",
...
h, e, l, l, o,
>>>

# 通过下标来循环打印，range是用来设置下标序号的。这里"0-4"
>>> range(len(str))
[0, 1, 2, 3, 4]
>>> for i in range(len(str)):
...     print str[i],
...
h e l l o
```

## range用法

> **原型：**range(start,stop,step)，其中**start**和**step**是可以省略的，开始值默认为0。
>
> **start：不存在时，默认为0。所以，range(i,j,1) = range(i,j)**
>
> **step：不存在时，默认为1，并且**必须**大于0**



> 1、range(i,j)，带有开始和结束，表示，range(i,j)=[i,i+1,i+2,i+3,...,j-1]
```python
>>> print range(1,5)
[1, 2, 3, 4]
```
> 2、range(j)，如果range只有一个参数，表示结束值，如：range(j)=[0,1,2,j-1]

```python
>>> print range(5)
[0, 1, 2, 3, 4]
```

> 3、range(i,j,2)，表示，range(i,j,2)=[i+2,(i+2)+2,(i+2+2)+2,...]
>


```python
>>> print range(1,10,2)
[1, 3, 5, 7, 9]
```
