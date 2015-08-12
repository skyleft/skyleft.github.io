---
layout: post
title: "Sendmail unqualified host name解决办法"
categories: "Linux"
tags: ["sendmail","sendmail错误","unqualified host name"]
---
帮朋友迁移网站，时候发现contact form发不了邮件了,

查看phpinfo,发现sendmail path 不正确，配置好之后，还是发送失败

查看sendmail日志 /var/log/mail.log，发现*unqualified host name (servername) unknown; sleeping for retry*之类的提示。

解决办法:
	servername代表server的hostname，请自行替换
	sudo vi /etc/hosts
	编辑或者加多一行
	127.0.1.1       servername.localhost servername

ok

---
