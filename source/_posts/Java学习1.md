---
title: Java学习(1):从Java特性到"Hello World!"程序
date: 2019-08-21 14:36:38
tags: 
 - Java
 - Programming
categories: Java
---

<head>
    <link href="https://cdn.bootcss.com/font-awesome/5.10.2/css/all.css" rel="stylesheet">
</head> 

> <i class = "fa fa-quote-left fa-3x fa-pull-left"></i>Java是一门后端程序员必须会的语言，在计算机历史中，它的各种独特的特性在计算机历史上留下了浓墨重彩的一笔。它的跨平台特性更是方便了广大的程序员朋友。  
> 那么，从今天开始，我们就开始学习Java这门厉害的语言吧!
<!--more-->

Java特性
===

1.  简单性：Java舍弃了C++中难以掌握不安全的功能如：指针、多继承等(Java语言底层是C++实现的)  
2.  面向对象：Java和C++一样，是一种面向对象编程语言
3. 安全性：如：运行时堆栈溢出，强制类型检查
4. 健壮性：Java语言在运行过程中产生的垃圾会自动回收,简称GC机制
5. 可移植性： Java程序编译一次,不做任何修改时到处运行,也就是跨平台（通过JVM实现）

JDK、JRE、JVM是什么
===

1. JDK：Java开发工具包，如果想开发Java程序则必须安装JDK,目前使用JDK12
2. JRE:java运行环境
3. JVM:Java虚拟机，如果想在操作系统上运行字节码文件，则必须有JVM

编写第一个Java程序"Hello World"
===

>我所使用的Java文件编辑器是VSCode，具体如何部署VSCode以用来编Java文件，请参考[官网链接](https://code.visualstudio.com/docs/java/java-tutorial)

1. 在自己的工作区目录下创建Java代码文件
    在java中，代码文件应命名为XXX.java.这里我的文件名称为:HelloWorld.java

2. 编写HelloWorld.java
    代码如下:

    ```java
    public class HelloWorld{
        public static void main(String[] args){
            System.out.println("Hello World!");
        }
    }
    ```

简单解释代码的意思
===

```java
    //public表示公开的
//class表示定义一个类
//HelloWorld表示一个类名
public class HelloWorld{//表示定义一个公开的类，叫做HelloWorld
    /*
        public表示公开的
        static表示静态的
        void表示空
        main表示方法名是main
        (String[] args) 是一个main方法的形式参数列表
    */
    //类体中不允许编写Java语句[除声明变量外]
    /*需要记住的是:
        以下的方法是一个程序的主方法，是程序的执行入口
        是规定的，固定的编写方式
    */
    public static void main(String[] args){//表示定义一个公开的静态的主方法
         /*
        方法体
        方法体
        方法体
         */

         //java语句[java语句以";"终止，分号必须是半角英语分号]
        System.out.println("Hello World!");//向控制台输出一段信息、消息
    }
} 
    ```
