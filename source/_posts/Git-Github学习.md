---
title: (更新中)Git&Github学习
date: 2019-08-16 10:58:13
tags: 
 - Git
 - Github
 - Blog
 - Programming
categories: 学习
---

<head>
    <script src="https://use.fontawesome.com/9c273aaf8d.js"></script>
</head> 

> <i class = "fa fa-quote-left fa-3x fa-pull-left"></i>Git和Github是所有程序员都需要了解并且会使用的工具，它们能很好地让你对软件/代码的版本进行控制、多人协同编辑代码、代码开源、代码发布等等。~~Github也是世界上最大的同性交友平台~~，无论如何，Git和Github都是一个合格的程序员需要了解的东西。那么今天就开始Git&Github的探索之旅
<!--more-->

Github学习
====

版本控制应该具有的功能
---

- 协同修改
   - 多人并行且不冲突地修改服务器端的同一个文件
- 数据备份
   - 不仅保存目录和文件的当前状态，还能够保存每一个提交过的历史状态
- 版本管理
  - 在保存每一个版本的文件信息的时候要做到不重复保存数据，以节约储存空间，提高运行效率。这方面SVN采用的是增量式管理的方式(只保存修改的部分)，而Github采用的是文件系统快照的方式。
- 权限控制
  - 对团队中参与的开发的人员进行权限控制
  - 对团队外开发者贡献的代码进行审核——Github独有的功能
- 历史记录
  - 查看修改人、时间、内容、日志信息
  - 将本地文件恢复到某一个历史状态
- 分支管理
  - 允许开发团队在工作过程中多条生产线同时推进任务，进一步提高效率

版本控制简介
---
### 版本控制

工程设计领域中使用版本控制管理工程蓝图的设计过程。在IT开发过程中也可以使用版本控制思想管理代码的版本更迭。

### 版本控制工具
版本控制工具主要分为两类，一类是集中式的版本控制工具，还有一类是分布式版本控制工具。

1. 集中式版本控制工具:  
CVS、SVN(使用的最多)、VSS
![集中式版本控制工具示意图](https://s2.ax1x.com/2019/08/16/mZ6S0g.png)
(容易出现单点故障——服务器宕机等，数据丢失)
2. 分布式版本控制工具:  
Git、Mercurial、Bazaar、Darcs……
![分布式版本控制工具示意图](https://s2.ax1x.com/2019/08/16/mZ6sjf.png)

Git简介
---

### Git简史
![分布式版本控制工具示意图](https://s2.ax1x.com/2019/08/16/mZcWqO.png)

### Git官网和Logo
<i class="fa fa-code-fork fa-lg"></i>[官网地址](https://git-scm.com/)  
> <i class="fa fa-code-fork fa-lg fa-pull-left"></i>Logo就是一个分支，能看出来Git的主打功能了吧XD

### Git的优势
- 大部分操作在本地完成，不需要联网
- 完整性保证（Hash算法）
- 尽可能添加数据而不是删除或修改数据
- 分支操作非常流畅
- 与Linux命令全面兼容
  
### Git安装
![第一步](https://s2.ax1x.com/2019/08/16/mZfLVK.png)
![第二步](https://s2.ax1x.com/2019/08/16/mZfbb6.png)
![第三步](https://s2.ax1x.com/2019/08/16/mZfX5D.png)
![第四步](https://s2.ax1x.com/2019/08/16/mZf7K1.png)
![第五步](https://s2.ax1x.com/2019/08/16/mZfHDx.png)
![第六步](https://s2.ax1x.com/2019/08/16/mZfOUO.png)
![第七步](https://s2.ax1x.com/2019/08/16/mZfvPe.png)

### Git的结构
![Git结构示意图](https://s2.ax1x.com/2019/08/16/mZo4Xj.png)  

### Git和代码托管中心
- 互联网环境下
  - Github
  - 码云
  - Coding
- 本地环境下
  - GitLab服务器

代码托管中心的任务:维护远程库

### 本地库与远程库
- 团队内部协作
![团队内部协作](https://s2.ax1x.com/2019/08/16/mZLnt1.png
)  
- 远程协作
![远程内部协作](https://s2.ax1x.com/2019/08/16/mZLmkR.png)

Git的命令行操作
---

### 本地库初始化

命令:`Git init`

效果:创建了一个`.git`目录

### 设置签名

- 形式:
  - 用户名:XXX
  - Email地址:1234@XX.com
- 作用:区分不同的开发人员身份
- 注意:这里设置的签名和登录远程库（代码托管中心）的账号密码没有任何关系
- 命令
  - 项目级别/仓库级别:仅在当前本地库范围内有效
    - git config XXX
    - git config 1234@XXX.com
  - 系统用户级别:登录当前操作系统的用户范围
    - git config <font style="color:red">**--global**</font> XXX
    - git config <font style="color:red">**--global**</font>  1234@XXX.com
  - 级别优先级
    - 就近原则:项目级别优先于系统用户级别，二者都有时采用项目级别
    - 不允许二者都没有

### 基本操作

1. 状态查看
   - ```bash
      git status
      ```
      查看工作区、暂存区状态  
2. 添加
   -  ```bash
       git add [file name]
      ```
      将工作区的新建或修改添加到暂存区  
3. 提交
   - ```bash
      it commit -m "commit message" [file name]
     ```
      将暂存区的东西提交到本地库  
4. 查看历史记录
   - ```bash
     git log
     ```
     ![效果示意图](https://s2.ax1x.com/2019/08/16/mmAALd.png)
     > 多屏显示控制方式
     > - 空格向下翻页
     > - b向上翻页
     > - q退出
   - ```bash
     git log --pretty=oneline
     ```
     ![效果示意图](https://s2.ax1x.com/2019/08/16/mmAksH.png)
   - ```bash
     git log oneline
     ```
     ![效果示意图](https://s2.ax1x.com/2019/08/16/mmA5OH.png)
   - ```bash
     git reflog
     ```
     ![效果示意图](https://s2.ax1x.com/2019/08/16/mmAj1S.png)
5. 版本的前进后退
   - 法一:基于索引值[推荐]
     ```bash
     git reset --hard [索引值]
     (此处的索引值可以用reflog中的缩减版)
     ```
   - 法二:基于^符号:只能往后退
     ```bash
     git reset --hard HEAD^ (退后一版)
     git reset --hard HEAD^^ (退后两版)
     git reset --hard HEAD^^^ (退后三版)
     ```
   - 法三:基于~符号:只能往后退
     ```bash
     git reset --hard HEAD~n (退后n版)
     ```
