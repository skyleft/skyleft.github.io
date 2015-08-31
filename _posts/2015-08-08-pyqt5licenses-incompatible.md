---
layout: post
title: "PyQt5编译提示licenses incompatible解决方法"
categories: "Python"
tags: ["Qt5","PyQt5"]
--- 
Mac OSX手动编译安装PyQt5，提示
*Error: This version of PyQt5 and the commercial version of Qt have incompatible licenses.*
解决方法：
	
	vi configure.py
	找到这一行if introspecting and target_config.qt_licensee != 'Open Source' and ltype == 'GPL':
	注释掉这一行和下面三行

ok
---
