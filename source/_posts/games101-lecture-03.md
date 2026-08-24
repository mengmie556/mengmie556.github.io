---
title: 'GAMES101 Lecture 03：Transformation'
date: 2026-02-20 10:03:00
updated: 2026-02-20 10:03:00
categories:
  - GAMES101
tags:
  - GAMES101
  - 计算机图形学
disableNunjucks: true
---

本文记录 GAMES101 第 03 讲的课程内容。

<!-- more -->
![Lecture 03 图 001](lecture-03-image-001.png)





## 二维变换：



缩放变换：

![Lecture 03 图 002](lecture-03-image-002.png)





对称变换

![Lecture 03 图 003](lecture-03-image-003.png)



切片（斜切）变换

![Lecture 03 图 004](lecture-03-image-004.png)



旋转变换

不说特殊点，就是绕着原点转，默认逆时针

![Lecture 03 图 005](lecture-03-image-005.png)

![Lecture 03 图 006](lecture-03-image-006.png)





二维线性变换的形式：

![Lecture 03 图 007](lecture-03-image-007.png)



## 齐次坐标

![Lecture 03 图 008](lecture-03-image-008.png)

原来的矩阵乘法公式不能表示平移变换，因为乘出来是ax+by的形式，而平移是x+a，y+b。因此还需要加东西，那么就不属于线性变换了。



但是一直这样写很麻烦，使得平移变换变成特殊变换了，那怎么统一呢？

齐次坐标：

![Lecture 03 图 009](lecture-03-image-009.png)

（相当于多开了一维储存常量）



![Lecture 03 图 010](lecture-03-image-010.png)

两个点相加会得到中点（因为矩阵把第三维加起来了，最后除以第三维权重的时候就除以了两倍权重，因此就变成中点了，主要就是权重翻倍但是坐标没有翻倍而是正常加了）



那么平移变换就可以表示为：

![Lecture 03 图 011](lecture-03-image-011.png)

其他几个变换就可以表示为：

![Lecture 03 图 012](lecture-03-image-012.png)



逆变换：

![Lecture 03 图 013](lecture-03-image-013.png)

（比较有意思的是，逆变换的变换矩阵就是原变换矩阵的逆，因此表示起来也是这样右上角加上-1）



![Lecture 03 图 014](lecture-03-image-014.png)

在真正进行变换计算的时候，我们要注意矩阵不是往右边写而是往左边写，同时要注意顺序，先做旋转再平移和先平移再旋转结果不同（也就是矩阵没有交换律），因此如图中先旋转再平移，我们的计算就是 （平移矩阵 * 旋转矩阵 * 原坐标）因为是从右边往左边算，所以最左边是最后的操作

![Lecture 03 图 015](lecture-03-image-015.png)



三维变换：

![Lecture 03 图 016](lecture-03-image-016.png)

（依旧考虑线性变换和平移的特殊情况啊，同样使用齐次坐标计算变换）



![Lecture 03 图 017](lecture-03-image-017.png)
