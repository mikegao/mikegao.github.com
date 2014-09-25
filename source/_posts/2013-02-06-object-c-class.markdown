---
layout: post
title: "Object-C 类、对象和方法"
date: 2013-02-06 11:33
comments: true
categories: object-c
---


``` objc 采用特定的语法对类和实例应用方法
[ClassOrInstance method];
// 在这条语句中，左方括号后要紧跟类的名称或者该类的实例的名称，它后面可以是一个或多个空格，空格后面是将要执行的方法。最后使用右方括号和结束分号来中止。

yourCar = [Car new];

[yourCar prep];     // 准备好第一次使用
[yourCar drive];    // 驾驶汽车
[yourCar wash];     // 洗车
[yourCar getGase];  // 如果需要就给汽车加油
[yourCar service];  // 维修

[yourCar topDown];  // 是否为一辆敞蓬车
[yourCar topUp];
currentMileage = [yourCar cruuentOdometer];
```

``` objc Interface
@interface NewClassName: ParentClassName
{
    memberDeclarations;
}
methodDeclarations;
@end

//---- @interface section ----
// 用于描述类、类的数据成分以及类的方法
@interface Fraction: NSObject{
    int numerator;
    int denominator;
}

-(void) print; // 开头的负号（-）通知编译器，这是一个实例方法 （+）表示为类方法
-(void) setNumberator: (int) n;
-(void) setDenominator: (int) d;

@end
```

``` objc Implementation
//---- @implementaion section ----
// 实现interface方法的实际代码
@implementation Fraction

-(void) print{
    NSLog(@"%i/%i", numerator, denominator);
}

-(void) setNumberator:(int)n{
    numerator = n;
}

-(void) setDenominator:(int)d{
    denominator = d;
}

@end
```

``` objc main 
Fraction *myFraction;  // myFraction用于存储来自新的Fraction类变量 （*）是必须的，表示myFraction是对Fraction的一个引用（或者指针）

// Create an instance of a Fraction
myFraction = [Fraction alloc];  // alloc是allocate的缩写，分配内存空间
myFraction = [myFraction init];
// 亦可写成
// myFraction = [[Fraction alloc] init];
// 最终简写形式
// Fraction *myFraction = [[Fraction alloc] init];
// 以上都扯淡
Fraction *myFraction = [Fraction new];

// Set fraction to 1/3
[myFraction setNumberator: 1];
[myFraction setDenominator: 3];

// Display the fraction using the print method

NSLog(@"The value of myFraction is:");
[myFraction print];

```