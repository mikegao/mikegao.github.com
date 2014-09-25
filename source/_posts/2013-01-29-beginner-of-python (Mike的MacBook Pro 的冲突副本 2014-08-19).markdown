---
layout: post
title: "Beginner_Of_Python"
date: 2013-01-29 10:42
comments: true
categories: python
---

``` python 变量交换
x = 6
y = 5

x, y = y, x
print x 
>>> 5
print y
>>> 6
```

``` python if 语句再行内
print "Hello" if True else "World"
>>> Hello
```
   
``` python 连接
# 下面的最后一种方式在绑定两个不同类型的对象时显得很cool
nfc = ["Packers", "49ers"]
afc = ["Ravens", "Patriots"]
print nfc + afc
>>> ['Packers', '49ers', 'Ravens', 'Patriots']

print str(1) + " world"
>>> 1 world

pring 1, "world"
>>> 1 world

print nfc, 1
>>> ['Packers', '49ers'] 1
```

``` python 数字技巧
# 除后向下取整
print 5.0//2
>>> 2
# 2的5次方
print 2**5
>>> 32
```

``` python 注意浮点数的除法
print .3/.1
>>> 2.9999999999999996
print .3//.1
>>> 2.0
```

``` python 数值比较
x = 2
if 3 > x > 1:
  print x
>>> 2
if 1 < x > 0:
print x
>>> 2
```

``` python 同时迭代两个列表
nfc = ['Packers', '49ers']
afc = ['Ravens', 'Patriots']
for teama, teamb in zip(nfc, afc)
print teama + " vs. " + teamb
>>> Packers vs. Ravens
>>> 49ers vs. Patriots
```

``` python 带索引的列表迭代
teams = ["Packers", "49ers", "Ravens", "Patriots"]
for index, team in enumerate(teams):
  print index, team
>>> 0 Packers
>>> 1 49ers
>>> 2 Ravens
>>> 3 Patriots
```

``` python 列表推导式
# 已知一个列表，我们可以刷选出偶数列表方法
numbers = [1,2,3,4,5]
even = [number for number in numbers if number%2 == 0]
```

``` python 字典推导
# 和列表推导类似
teams = ['Packers', '49ers', 'Ravens', 'Patriots']
print {key: value for value, key in enumerate(teams)}
>>> {'49ers': 1, 'Ravens': 2, 'Patriots': 3, 'Packers': 0}
```

``` python 初始化列表的值
items = [0]*3
print items
>>> [0, 0, 0]
```

``` python 列表转换为字符串
teams = ['Packers', '49ers', 'Ravens', 'Patriots']
print ", ".join(teams)
>>> 'Packers, 49ers, Ravens, Patriots'
```

``` python 从字典中获取元素
data = {'user': 1, 'name': 'Max', 'three': 4}
try:
  is_admin = data['admin']
except KeyError:
  is_admin = False
# 替换成这样：
data = {'user': 1, 'name': 'Max', 'three': 4}
is_admin = data.get('admin', False)
```

``` python 获取列表的子集
x= [1,2,3,4,5]
# 前3个
print x[:3]
>>> [1, 2, 3]
# 中间4个
print x[1:5]
>>> [2, 3, 4, 5]
# 最后3个
print x[3:]
>>> [4, 5, 6]
# 奇数项
print x[::2]
>> [1, 3, 5]
# 偶数项
print x[1::2]
>> [2, 4, 6]
```

``` python 60个字符解决FizzBuzz
# 写一个程序，打印数字1到100，3的倍数打印“Fizz”来替换这个数，5的倍数打印“Buzz”，对于既是3的倍数又是5的倍数的数字打印“FizzBuzz”
for x in range(101):print'fizz'[x%3*4::]+'buzz'[x%5*4::]or x
```

``` python 集合
from collections import Counter
print Counter("hello")
>>> Counter({'1': 2, 'h': 1, 'e': 1, 'o': 1})
```

``` python 迭代工具
# 和collections库一样，还有一个库叫itertools，对某些问题真能高效地解决。其中一个用例是查找所有组合，他能告诉你在一个组中元素的所有不能的组合方式
from itertools import combinations
teams = ["Packers", "49ers", "Ravens", "Patriots"]
for game in combinations(teams, 2):
print game
>>> ('Packers', '49ers')
>>> ('Packers', 'Ravens')
>>> ('Packers', 'Patriots')
>>> ('49ers', 'Ravens')
>>> ('49ers', 'Patriots')
>>> ('Ravens', 'Patriots')
```

``` python False == True
False = True
if False:
  print "Hello"
else:
  print "World"
>>> Hello
```
