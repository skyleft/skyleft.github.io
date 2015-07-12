---
layout: post
title: "tomcat中指定maven profile"
categories: "java"
tags: ["java", "tomcat", "maven"]
---

Maven中的profile可以很好的实现不同的运行时环境加载不同配置文件这种需求，
但是如果不使用maven的tomcat插件，而是直接在eclipse的server中启动tomcat，
如何去指定使用的是哪一个profile呢？
其实很简单，看了下面这张图就知道了，具体做法就是 在项目上右键 -- properties -- maven,
然后右边 Active Maven Profile 中，输入想要运行的profile即可。

![tomcat指定maven profile](/assets/images/QQ20150712-1@2x.png)

---
