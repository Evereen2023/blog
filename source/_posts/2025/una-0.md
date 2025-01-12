---
title: Una博客：一个博客诞生的故事
description: 看到纸鹿写的博客如此好看，令我羡慕不已，刚好不知道改做些什么项目，于是刚刚拥有唤青映记的我决定抄袭（bushi）纸鹿的代码，使用Nuxt写一个新博客。代号——Una。
date:
updated:
categories: [Una]
type: story
---

{% note color:orange 前言 看到纸鹿写的博客如此好看，令我羡慕不已，刚好不知道改做些什么项目，于是刚刚拥有唤青映记的我决定抄袭（bushi）纸鹿的代码，使用nuxt写一个新博客。代号——Una。 %}

## 就这么，开始了？

在2025年1月1日的下午，我向纸鹿发送了一条消息

{% quot 我打算用astro做一个博客试试 %}

由此便开启了我的新博客制作。

### 从Astro入手

所以，为什么最开始的我在众多的框架里选择了Astro呢？在有了自己造一个新博客的想法以后，我便着手选择起了框架，最终，我在纸鹿的博客里读到了这篇文章

{% link https://blog.zhilu.cyou/2024/blog-using-nuxt#%E9%87%8D%E6%9E%84%E6%80%9D%E8%80%83  博客进化：从 Hexo 到 Nuxt Content icon:https://www.zhilu.cyou/api/avatar.png desc:false %}

看到他这么说，我毫不犹豫的选择了Astro。

### Astro的新手教程

Astro的新手教程绝对是我见过最详细的了，它会带着你写一个基础的小博客，以让你熟悉一些Astro的基本功能

{% link https://docs.astro.build/en/tutorial/0-introduction/  Build your first Astro Blog desc:false %}

在示例的引导下，我摸索着写出了一个简单的小框架。

{% gallery layout:flow %}
![文章列表](https://img.miasite.com/local/api/1/2025/01/1736614147583.png)
![分类列表](https://img.miasite.com/local/api/1/2025/01/1736614151235.png)
{% endgallery %}

第二天，我不断的尝试于更改之下，做出了

{% image https://img.miasite.com/local/api/1/2025/01/1736614483489.png %}

{% link https://unsplash.com/photos/snow-field-during-daytime-H9m6mfeeakU  背景图片出自Unsplash desc:false %}

## 抛弃Astro，拥抱Nuxt

经历了两天开发的快感之后，我突然发现——Astro不适合我。

### 怎么就突然反水了呢？

在第二天，因为一些bug，我习惯性的去找纸鹿询问

{% image https://img.miasite.com/local/api/1/2025/01/1736615396322.png %}

是的，这片对话让我意识到，纸鹿并没有怎么使用过Astro，却用Nuxt开发了自己的博客，一定积累了许多的经验，再加上我喜欢Vue，而Nuxt与Vue的结合程度非常高。这时我的脑海里不禁想起

{% quot 适合自己的才是最好的 %}

于是我毅然决然转向了Nuxt。

### 开启快乐的“抄袭”之旅

我将原有的代码迁移至nuxt，给新博客起了个代号“Una”（下文使用“Una”代替“新博客”），简单看了一下Nuxt的文档，写的有些简陋。转头望向纸鹿的博客，打开源码，开抄 :)

新建一个app文件夹，将原来在根目录下的部分文件迁移过去，Nuxt在命令行里疯狂报错，上网搜寻良久，无果，可纸鹿的博客又能正常运行，于是向纸鹿询问。

{% image https://img.miasite.com/local/api/1/2025/01/1736694143424.png %}

得知这是Nuxt3迁移Nuxt4的实验性功能，查阅官网，终于在一个不起眼的地方发现了它

{% link https://nuxt.com/docs/getting-started/upgrade#opting-in-to-nuxt-4 Opting in to Nuxt4 desc:false %}

添上
{% box child:codeblock color:green %}
```json
future: {
    compatibilityVersion: 4,
},
```
{% endbox %}

遂得Nuxt4。

同时受到纸鹿的启发，我也将Una的公共配置放在了una.blog.vonfig.ts里进行统一处理。又因为本人比较喜欢winui3的设计，于是引入了侧边栏与顶栏。

截至2025/01/12，已经完成了基本的布局。

{% gallery layout:flow %}
![文章列表](https://img.miasite.com/local/api/1/2025/01/1736695062962.png)
![分类列表](https://img.miasite.com/local/api/1/2025/01/1736695075637.png)
{% endgallery %}

<!-- 在文末，附上Una Blog的时间轴

{% timeline %}
<!-- node 2025年 1月 1日 -->
开始制作Astro版本的新博客，完成基本布局。
{% endtimeline %} -->