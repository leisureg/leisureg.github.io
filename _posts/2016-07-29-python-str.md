---
layout: post
title: str集
categories: python
tags: str
---

* content
{:toc}

# str集

> **1.去除空格。**
>
> `原型：str.strip()`		
>
> 功能：去除字符串**前后**的空格。

```python
>>> test=' hello,world '
>>> test
' hello,world '
>>> test=test.strip()
>>> test
'hello,world'
```

> **2.获取字符串长度。**
>
> `原型：len(str)`	
>
> 功能：根据字符串内容获取长度。
>
> *注意：这里len(object)，`object`也可以是`list对象`，这时代表list的对象个数*

```python
>>> test='leisureg'
>>> num=len(test)
>>> num
8
```

> 3.输出指定字符串
>
> `原型：str[n:m]`=str[n],str[n+1],...,str[m-1]
>
> 功能：从一个字符串中，输出指定的字符串或字符。
>
> n与m，分别代表字符串的下标，数组默认从0开始，所以最大长到m-1个字符。
>
> n不存在时，代表从0开始，也就是从字符起始位置开始，
>
> m不存在时，代表输出到字符结束。

```python
# 字符串原型
>>> test
'leisureg'

# 输出从开始到i的字符串
>>> test[0:3]
'lei'
>>> test[:3]
'lei'

# 输出e到s的字符串
>>> test[1:4]
'eis'

# 输出s到结尾的字符串
>>> test[3:]
'sureg'
```



