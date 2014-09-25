---
layout: post
title: "Object-C 数据类型和表达式"
date: 2013-02-06 14:13
comments: true
categories: object-c
---

##I. Int类型

###1.八进制
如果第一位是0，则表示8进制
NSlog调用格式字符串使用格式符号%o，显示的值不带有前导0，使用%#o将显示前导0
###2.十六进制
0x开头表示16进制
``` objc
rgbColor = 0xFFEF0D;
```
NSlog调用格式字符串使用格式符号%x，显示的值不带有前导0x，使用%#X或%X将显示前导0x

##II. Float类型
要使用科学计数法，NSLog格式字符串中指定格式字符%e，使用NSLog格式字符串%g允许NSLog确定使用常用的浮点计数法

###III. Double类型
要显示double值，可用格式符号%f, %e或%g，它们与显示float值所用的格式符号是相同的。

###IV. char类型
将字符放入一对单引号中就能得到字符常量
字符常量是放在单引号中的单个字符，字符串则是放在双引号中的任意个字符。前面有@字符并且放在双引号中的字符串是NSString字符串对象。
在NSLog调用中可以使用格式字符%c。


``` objc 
int intergerVar = 100;
float floatingVar = 331.79;
double doubleVar = 8.44e+11;
char charVar = 'W';

NSLog(@"integerVar = %i", integerVar);
NSLog(@"floatingVar = %f", floatingVar);
NSLog(@"doubleVar = %e", doubleVar);
NSLog(@"doubleVar = %g", doubleVar);
NSLog(@"charVar = %c", charVar);
```

``` objc
long int numberOfPoints = 131071100L;
NSLog(@"long int = %li", numberOfPoints);

short int number = 123;
NSLog(@"shot int = %hi", number);

unsigned int counter; // 变量counter只用于保存正值
//0x00ffU
200000UL //将常量20000看作unsigned long
```

``` objc
-(id) newObject: (int) type; // 声明一个名为newObject的实例方法，它具有名为type的单个整型参数并有id类型的返回值。
```

