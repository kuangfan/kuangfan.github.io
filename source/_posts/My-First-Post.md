---
title: 博客简述
date: 2019-12-13 15:06:11
tags:
- 随笔
- 心得
---
欢迎来到我的个人博客。我将在这里分享一些前端的工作经验与心得，记录一些平时工作中遇到的问题以及对应解决方案，以及把前端的知识体系重新梳理一遍。

## 为什么要写博客？

本人作为一名前端从业者已经快6个年头，以前从来没有过写博客的习惯。每天写代码都已经够累了，基本一下班回到家就想要放松放松，看看视频打打游戏，周末也基本是一觉睡到中午或者出去玩。以至于工作了这么多年都感觉没有什么积累，永远都是用完就忘了。现在记忆力也越来越差了，很多上一秒还在想的事情下一秒很可能就忘了，还是得养成记录的良好习惯才行。

再一个原因就是，现在的从事前端工作的人越来越多了，各种培训班、其他行业转岗的以及计算机专业的学生，有些牛人甚至还没毕业就有自己的开源项目了，竞争可想而知越来越激烈了。再加上所谓的“互联网寒冬”，各种大公司纷纷裁员，市场行情也没以前好了。前端的各种技术、框架层出不穷，要掌握的知识面也越来越广了。现在招人的大多数也不缺初中级前端，面试基本都会问你各种底层原理源码实现的相关问题。

所以想要脱颖而出，把自己提升一个档次，拿到更高的工资，不能再做一个切图仔、架子工、API工程师了。以前比较浮躁，学习东西都浮在表面看完就感觉自己会了，从现在起一步一个脚印把过去所学的东西系统化的重新梳理一遍，把知识点串联起来吃透，打牢基础，理解记忆。学习虽然很枯燥很痛苦，但远比以后后悔来的轻。

大家可以一起来写博客，互相学习，把掌握的知识通过自己的理解写出来记忆更加深刻，也方便以后复习的时候直接拿来看更加快捷，看自己写的东西一下子就能回忆起来当时的想法。
废话不多说，一起加油努力吧！

## 那么怎样写一个这样的博客呢？

最简单最快速的方法就是用GitHub Pages来搭建，而且不用花钱。本博客就是使用Hexo + GitHub Pages来搭建的，下面简单介绍一下搭建的流程，供大家参考。

### 环境准备
- [node.js](https://nodejs.org/en/)(Node.js 版本需不低于 8.10，建议使用 Node.js 10.0 及以上版本)
- [git](https://git-scm.com/)

### Hexo搭建
安装 [Hexo](https://hexo.io/zh-cn/docs/)，打开 Git Bash 命令窗口，输入命令：
``` bash
$ npm install -g hexo-cli
```
安装好 Hexo 后，建一个博客项目的文件夹，然后进入这个文件夹，在命令行输入命令：
``` bash
$ hexo init
```
执行完成后会在项目文件夹下生成文件结构，然后安装一下依赖：
``` bash
$ npm install
```
依赖包下载完成后，输入如下命令启动 hexo 的内置 Web 服务器：
``` bash
$ hexo g // 打包文件
$ hexo s // 启动服务器
```
然后可以在浏览器中通过地址 http://localhost:4000/ 访问博客了。

根目录下的_config.yml为网站的[配置信息](https://hexo.io/zh-cn/docs/configuration)，您可以在此配置大部分的参数

### 更换主题
Hexo主题可以去这里找：https://hexo.io/themes/。更换主题的方式很简单，只需要将主题文件拷贝至根目录下的 themes 目录中，然后修改根目录下 _config.yml 文件中的 theme 字段，便可完成更换。
例如本博客使用的主题：https://github.com/jerryc127/hexo-theme-butterfly

在博客项目的根目录下，输入命令：
``` bash
$ git clone https://github.com/jerryc127/hexo-theme-butterfly.git
```
这个主题比较特殊还需要执行如下命令安装一些依赖：
``` bash
$ npm install hexo-renderer-pug hexo-renderer-stylus --save
```
打开根目录下的_config.yml文件，将theme字段的值修改为Butterfly。
``` bash
# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
theme: Butterfly
```
然后重新执行打包命令重启服务器，刷新浏览器就能看到不一样的效果了。
注：在项目文件中存在两个_config.yml文件，为了方便区分。
- 项目根目录下的 _config.yml 文件叫作站点配置文件。
- 主题文件夹根目录下的 themes/Butterfly/_config.yml 文件叫作主题配置文件。

### 部署到GitHub Pages
在github上新建一个仓库，仓库名必须是：<GitHub 账号名称>.github.io，这是GitHub pages 的特殊命名规范

Hexo提供了快速方便的一键部署功能，让您只需一条命令就能将网站部署到服务器上。
安装hexo-deployer-git：
``` bash
$ npm install hexo-deployer-git --save
```
修改根目录下的_config.yml文件
``` bash
# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: 'git'
  repo: 
    github: https://github.com/kuangfan/kuangfan.github.io.git
  branch: master
```
然后打包进行部署：
``` bash
$ hexo g
$ hexo d
```
部署成功后，在浏览器访问网址：https://<GitHub 账号名称>.github.io 即可查看博客。

大功告成，开始写文章吧。Markdown语法参考https://www.runoob.com/markdown/md-tutorial.html。

