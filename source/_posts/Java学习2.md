---
title: Java学习(2):关于Java语言中的标识符
date: 2019-08-21 19:18:23
tags: 
 - Java
 - Programming
categories: 学习
---
<!--more-->

什么是标识符？
===

<font color = "orange" style = "font-size: 16px">**在Java源程序当中凡是程序员有权利自己命名的单词都是标识符**</font>  

标识符可以标识什么元素呢  
- 类名
- 方法名
- 变量名
- 接口名
- 常量名
- ……等等

标识符的命名规则？
===

> 如果不按照命名规则来，编译器会报错，这是规定语法

1. 一个合法的标识符只能由"数字、字母、下划线(_)、美元符号($)"组成
2. 标识符不能以数字开头
3. 标识符要严格区分大小写
4. 关键字(public class static void等等)不能做标识符
5. 理论上标识符无长度限制，但是最好不要太长


|    合法     |   不合法    |
| :---------: | :---------: |
|  _123Test   |   123Test   |
| HelloWorld  | HelloWorld! |
| HelloWorld_ | HelloWorld# |
|    A_B_C    |    A B C    |
|    $ABC     |    1ABC     |
|   class1    |    class    |

标识符的命名规范
===
> 命名规范不是规则，可以不遵守，不遵守也不会报错

1. 最好见名知意
    - ~~a123~~、~~b456~~、~~c789~~
    - SystemService、studentNumber、lineHeight
2. 遵守驼峰命名法
    - 类名、接口名:首字母大写，后面每个单词首字母大写。
    - 变量名、方法名:首字母小写，后面每个单词首字母大写
    - 常量名:全部大写
    - SystemService、CustomService、studentNumber、lineHeight、PI、MAXSIZE
