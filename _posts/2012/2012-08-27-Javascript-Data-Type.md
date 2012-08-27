---
layout: post
published: true
categories:javascript
title:Javascript 数据类型
---

# Javascript 数据类型 #

## 1.Undefined类型 ##
Undefined类型只有一个值，即undefined。一个声明但未初始化的变量的值就是undefined。它与未声明的变量不同，不过`typeof`对未声明和未初始化的变量的返回值都是undefined。

## 2.Null类型 ##
Null类型也只有一个值，即null。它表示一个**空对象**指针（注意理解“空对象”，再看看这个域名，再联想下楼主状态… -_-|||），因此`typeof null`返回值为object。如果定义的变量将用于保存对象，那么最好将变量初始化为null。由于undefined值派生自null值，所以：
> `alert(null == undefined);  //true`

## 3.Boolean类型 ##
Boolean类型有两个值：true和false。注意：True和False不是Boolean类型值，而是标示符。下面这些值调用转型函数Boolean()都是返回false：

- false
- ""（空字符串）
- 0和NaN
- null
- undefined

## 4.Number类型 ##

1. 浮点数值的内存空间是整数值得两倍；
2. `0.1+0.2=0.3000000000000000004`（这是基于IEEE754浮点计算的通病）；
3. NaN(Not a Number)用来表示一个应该返回数值的操作符未返回数值的情况，例如除零的返回值就是NaN；NaN不与任何值相等，包括自己；检测函数isNaN()在检测对象时，会先调用对象的`valueOf()`方法，尝试转换该返回值，如不能转换，则调用该返回值的`toString()`方法，并尝试转换它的返回值。
4. `Number("")  //0`，而`parseInt("")  //NaN`；parseInt()可加第二个参数指定进制；ECMAScript 3和ECMAScript 5在解析八进制时存在歧义。

## 5.String类型 ##
String类型表示由零个或多个16位Unicode字符组成的字符序列。字符串是不可变的。（疑问：这和C#是一样的，但既然JS没有提供类似StringBuilder的类型，那JS是如何处理大量的String拼接的问题的呢？两者的GC处理有何异同呢？）

## 6.Object类型 ##
ECMAScript中的对象是一组数据和功能的集合。Object是所有对象的基础。Object类型的每个实例都具有以下属性和方法：

- Constructor: 保存创建当前对象的函数
- hasOwnProperty(*propertyName*): 检测给定属性是否存在当前对象中，而不是在当前对象的原型中
- isPrototypeOf(object)
- propertyIsEnumerable(*propertyName*)
- toLocaleString()
- toString()
- valueOf()

关于Object类型，将在后面的面向对象文章中详细介绍。

--EOF--