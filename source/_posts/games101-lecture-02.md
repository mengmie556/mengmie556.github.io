---
title: 'GAMES101 Lecture 02：线代复习'
date: 2026-02-20 10:02:00
updated: 2026-02-20 10:02:00
categories:
  - GAMES101
tags:
  - GAMES101
  - 计算机图形学
disableNunjucks: true
---

本文记录 GAMES101 第 02 讲的课程内容。

<!-- more -->
![Lecture 02 图 001](lecture-02-image-001.png)

向量相加，平行四边形法则和三角形法则







![Lecture 02 图 002](lecture-02-image-002.png)



这样定义方便进行计算向量长度



![Lecture 02 图 003](lecture-02-image-003.png)

点乘定义：a模 * b模  * cosx

通过转换可以快速求出两个向量间的夹角大小

当两个向量都是单位向量的时候，点乘直接等于夹角的余弦值



![Lecture 02 图 004](lecture-02-image-004.png)

点乘式子的含义其实是求一个向量在另一个向量上的投影



![Lecture 02 图 005](lecture-02-image-005.png)

因此可以快速求出垂直的向量（b-bp，因为bp是b在a上的投影，那么我此时b肯定是矩形对角线了，也就是说，那条虚线肯定是垂直的）



![Lecture 02 图 006](lecture-02-image-006.png)

a和b更近，那a和b点乘就接近1，然后远离到垂直就是0，再远离就是-1。





![Lecture 02 图 007](lecture-02-image-007.png)

点乘运算律



![Lecture 02 图 008](lecture-02-image-008.png)

叉乘能快速算出一个与两个向量都垂直的向量，图中的算式只是算了a 叉乘 b 的大小，没有方向，方向根据右手定则判定（四指是旋转方向，如果a 叉乘 b ，那就是四指从a方向 旋转 到b方向这样弯曲，此时大拇指指向的方向就是我们想求的一个向量的方向）



![Lecture 02 图 009](lecture-02-image-009.png)

叉积的运用，判定左右内外



![Lecture 02 图 010](lecture-02-image-010.png)

左边的图：右手坐标系，a 叉乘 b得到正的z，那么说明b在a左边，同理b叉乘a得到负z，那么a就在b右边



右边的图：依次进行AB 叉乘 AP，BC叉乘BP，CA叉乘CP，都得到正的z轴，说明p在AB，BC，CA左边，因此P在三角形内部，只要有一个叉乘计算出p在某条边右边，那就是P在三角形外部（换句话说，就是如果能判断点在三角形三条边的方向都相同，那就是内部，否则是外部）



一些叉乘的计算律

![Lecture 02 图 011](lecture-02-image-011.png)



![Lecture 02 图 012](lecture-02-image-012.png)

通过点乘叉乘计算出一个坐标系（两两相点乘为0，说明两两之间相互垂直，w又是u叉乘v得到的方向，因此与u，v所在平面垂直）



矩阵



![Lecture 02 图 013](lecture-02-image-013.png)

快速计算最终矩阵某个位置的方法，如果我要计算26，也就是第二行第四列的值，那我们找第一个矩阵的第二行和第二个矩阵的第四列，然后点乘求和就行（4 * 5 + 2 * 3）.



![Lecture 02 图 014](lecture-02-image-014.png)

矩阵的转置



![Lecture 02 图 015](lecture-02-image-015.png)

点乘和叉乘的矩阵表示



![Lecture 02 图 016](lecture-02-image-016.png)

矩阵的运算律
