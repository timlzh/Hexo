---
title: （更新中）Markdown学习笔记(2):Markdown进阶
date: 2019-08-14 20:44:57
tags: 
 - Markdown
 - Blog
 - Programming
categories: 学习
---
<head>
    <link href="https://cdn.bootcss.com/font-awesome/5.10.2/css/all.css" rel="stylesheet">
</head> 

> <i class="fa fa-quote-left"></i>Markdown真好用！<i class="fa fa-quote-right"></i>

<!--more-->

---

使用[Font Awesome](https://fontawesome.com/icons?d=gallery "Font Awesome")美化Markdown
===

> <i class="fa fa-quote-left fa-3x fa-pull-left"></i>在Markdown中，我们时常要调用一些小图片，而这些小图片如果去网上找或者上传图床会十分的麻烦。此时，一种一站式解决方案出现了——Font Awesome  
> Font Awesome是一个图标站，并且可以方便的调用刀Markdown、HTML中，所以这是一个很强大的工具。今天就来学习一下在Markdown语言中Font Awesome的用法


Font Awesome基础
---

### 添加图标

效果:

<i class="fab fa-weixin"></i> 我的微信

使用方法:  
**第一步:在[Font Awesome的CDN站](http://www.fontawesome.com.cn/get-started/)注册并获取自己的js文件** 

> 这里使用CDN站是因为Font Awesome的主站在国内访问比较慢，CDN站速度会快很多

之后,我们便获取了一个专属的js文件
```HTML
    <script src="https://use.fontawesome.com/你的专属码.js"></script>
```

**第二步:将这个js文件插入Markdown文件**
```HTML
    <head> 
        <script src="https://use.fontawesome.com/你的专属码.js"></script>
    </head> 
```
我们需要将上面这段代码插入Markdown文件的任意位置

**第三步:在文章中调用图标文件**

我们可以去[FontAwesome官网](https://fontawesome.com/icons?d=gallery)找到心水的图标

```HTML
    <i class="fab fa-weixin"></i> 我的微信
```

### 放大图标


**方法一:使用fa-nx放大**  
效果:  
<i class = "fab fa-weixin"></i>1x
<i class = "fab fa-weixin fa-lg"></i>133%
<i class = "fab fa-weixin fa-2x"></i>2x
<i class = "fab fa-weixin fa-3x"></i>3x

代码:
```HTML
<i class = "fab fa-weixin"></i>1x
<i class = "fab fa-weixin fa-lg"></i>133%
<i class = "fab fa-weixin fa-2x"></i>2x
<i class = "fab fa-weixin fa-3x"></i>3x
缺点:最高支持五倍放大
```


**方法二:使用font-size放大**  
效果:  
<i class = "fab fa-weixin" style = "font-size: 10px"></i>10px
<i class = "fab fa-weixin" style = "font-size: 30px"></i>30px
<i class = "fab fa-weixin" style = "font-size: 50px"></i>50px

代码:
```HTML
<i class = "fab fa-weixin" style = "font-size: 10px"></i>10px
<i class = "fab fa-weixin" style = "font-size: 30px"></i>30px
<i class = "fab fa-weixin" style = "font-size: 50px"></i>50px
优点:无限放大
缺点:麻烦
```

Font Awesome进阶
---

### 图标上色

效果:

<i class = "fab fa-weixin fa-2x" style = "color:red"></i>红    
<i class = "fab fa-weixin fa-2x" style = "color:green"></i>绿
> 死亡配色...

代码:
```HTML
<i class = "fab fa-weixin fa-2x" style = "color:red"></i>红    
<i class = "fab fa-weixin fa-2x" style = "color:green"></i>绿
```

### 让图标动起来
效果:

<i class = "fa fa-spinner fa-2x fa-spin"></i>连续的旋转  
<i class = "fa fa-spinner fa-2x fa-pulse"></i>八帧旋转

代码
```HTML
<i class = "fa fa-spinner fa-2x fa-spin"></i>连续的旋转  
<i class = "fa fa-spinner fa-2x fa-pulse"></i>八帧旋转
```

附:常用的旋转图标  
<i class = "fa fa-spinner fa-spin"></i>加载图标1`<i class = "fa fa-spinner fa-spin"></i>`  
<i class = "fa fa-circle-o-notch fa-spin"></i>加载图标2`<i class = "fa fa-circle-o-notch fa-spin">`  
<i class = "fa fa-cog fa-spin"></i>设置图标`<i class = "fa fa-cog fa-spin">`  
<i class = "fa fa-refresh fa-spin"></i>刷新图标`<i class = "fa fa-refresh fa-spin">`  

### 图标下沉(文字环绕)

效果（此处引用开头的代码）:
> <i class="fa fa-quote-left fa-3x fa-pull-left"></i>在Markdown中，我们时常要调用一些小图片，而这些小图片如果去网上找或者上传图床会十分的麻烦。此时，一种一站式解决方案出现了——Font Awesome  
> Font Awesome是一个图标站，并且可以方便的调用刀Markdown、HTML中，所以这是一个很强大的工具。今天就来学习一下在Markdown语言中Font Awesome的用法

代码
```HTML
> <i class="fa fa-quote-left fa-3x fa-pull-left"></i>在Markdown中，我们时常要调用一些小图片，而这些小图片如果去网上找或者上传图床会十分的麻烦。此时，一种一站式解决方案出现了——Font Awesome  
> Font Awesome是一个图标站，并且可以方便的调用刀Markdown、HTML中，所以这是一个很强大的工具。今天就来学习一下在Markdown语言中Font Awesome的用法
```

### 图标加边框

效果  
<i class="fa fa-quote-left fa-border"></i>

代码
```HTML
<i class="fa fa-quote-left fa-border"></i>
```

### 图标的旋转与翻转

**旋转**  
效果  
<i class="fa fa-arrow-up"></i>上箭头  
<i class="fa fa-arrow-up fa-rotate-90"></i>左箭头  
<i class="fa fa-arrow-up fa-rotate-180"></i>下箭头  
<i class="fa fa-arrow-up fa-rotate-270"></i>右箭头  

代码  
```HTML
<i class="fa fa-arrow-up"></i>上箭头  
<i class="fa fa-arrow-up fa-rotate-90"></i>左箭头  
<i class="fa fa-arrow-up fa-rotate-180"></i>下箭头  
<i class="fa fa-arrow-up fa-rotate-270"></i>右箭头  
```

**翻转**  
效果  
<i class="fa fa-envira"></i>普通  
<i class="fa fa-envira fa-flip-horizontal"></i>左右翻转  
<i class="fa fa-envira fa-flip-vertical"></i>上下翻转  

代码  
```HTML
<i class="fa fa-envira"></i>普通  
<i class="fa fa-envira fa-flip-horizontal"></i>左右翻转  
<i class="fa fa-envira fa-flip-vertical"></i>上下翻转
```

### ~~图标的堆叠~~

效果: 
  
<span class="fa-stack">
<i class="fa fa-camera fa-stack-1x"></i>
<i class="fa fa-ban fa-stack-2x" style = "color:red"></i>
</span>
禁止拍照

> 由于melody主题的问题，不能正常显示

代码:   
```HTML  
<span class="fa-stack [此处使用fa-nx或fa-lg可以整体放大]">
  <i class="fa fa-camera fa-stack-1x(较小图标)"></i>
  <i class="fa fa-ban fa-stack-2x(较大图标)" style = "color:red"></i>
</span>
禁止拍照
```
