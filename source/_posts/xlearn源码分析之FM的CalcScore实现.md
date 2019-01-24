---
title: xlearn源码分析之FM的CalcScore实现
date: 2019-01-24 12:15:21
tags: 
 - C++
 - xlearn
categories: xlearn
mathjax: true
---

## 写在前面

xlearn是由Chao Ma实现的一个高效的机器学习算法库，这里附上github地址：

https://github.com/aksnzhy/xlearn

FM是机器学习中一个在CTR领域中表现突出的模型，最早由Konstanz大学Steffen Rendle（现任职于Google）于2010年最早提出。

## FM模型



$$y(\mathbf{x}) = w_0+ \sum_{i=1}^n w_i x_i + \sum_{i=1}^n \sum_{j=i+1}^n w_{ij} x_i x_j​$$



$$y(\mathbf{x}) = w_0+ \sum_{i=1}^n w_i x_i + \sum_{i=1}^n \sum_{j=i+1}^n \langle \mathbf{v}_i, \mathbf{v}_j \rangle x_i x_j$$













