---
layout: post
title: list与str
categories: python
tags: list str
---

* content
{:toc}

# list与str的区别

## 相同点

1.都可以通过下标获取指定数据。

```python
>>>first="test"
>>>first[0]
't'

>>>first=['test','test2','test3']
>>>first[0]
'test'
```

   ​

2.都具有用`str1+str2`来连接两个同类型的变量。

```python
>>>first="test"
>>>second="test2"
>>>first+second
'testtest2'

>>>first=['1','2']
>>>second=['3','4']
>>>first+second
['1','2','3','4']
```

   ​

3.`value[:n]`通过这种方式获取指定数据,偏移量从`0`开始，到总元数`n-1`结束。

```python
>>>first=['test','test2','test3']
>>>first[:2]
['test','test2']

>>>second="test23"
>>>second[:2]
'te'
```

4.`len`获取元素数或字符串数

```python
>>>first=['1','2','3']
>>>len(first)
3

>>>first="1234567"
>>>len(first)
7
```

## 不同点

> list与str最大的区别就是：list是可以改变的，str是不可变。
>
> 如果要修改str中的元素，可以创建一个新的str，来实现他的改变。

```python
>>> first=['1','2','3','4']

# 追加元素
>>> first.append('5')
>>> first
['1', '2', '3', '4', '5']

# 修改元素
>>> first[0]
'1'
>>> first[0]='test'
>>> first[0]
'test'

# 插入元素
>>> first.insert(1,"hello")
>>> first
['test', 'hello', '2', '3', '4', '5']

# 删除元素
>>> del first[1]
>>> first
['test', '2', '3', '4', '5']
```

**以上这些操作在`str`中都会失败。**

## list多维使用

> list中的元素可以是任何类型的数据：

```python
>>> matrix=[[1,2,3],['a','b','c'],'d',5]
>>> print matrix
[[1, 2, 3], ['a', 'b', 'c'], 'd', 5]
>>> matrix[0]
[1, 2, 3]
>>> matrix[0][1]
2
>>> matrix[2]
'd'
```

## list和str转化

> `str.split()`可以将str转化为list。

```python
# 采用"."作为分隔符
>>> line="hello. I am leisureg.welcome you."
>>> line.split(".")
['hello', ' I am leisureg', 'welcome you', '']
>>> list=line.split(".")
>>> list
['hello', ' I am leisureg', 'welcome you', '']

# 根据"."被作为分隔符的个数，来划分
>>> list=line.split(".",1)
>>> list
['hello', ' I am leisureg.welcome you.']

# 如果split()在不输入任何参数的情况下，见到任何分隔符号，就用其分割。
>>> str="I am,writing\npython\tbook on line"
>>> str
'I am,writing\npython\tbook on line'
>>> print str
I am,writing
python  book on line
>>> str.split();
['I', 'am,writing', 'python', 'book', 'on', 'line']
>>>
```

> `"".join(list)`将str转化为list。

```python
>>> list=['hello','world']
>>> list
['hello', 'world']
>>> "".join(list)
'helloworld'
>>> ".".join(list)
'hello.world'
>>> " ".join(list)
'hello world'
```