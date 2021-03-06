---
layout: post
title:  Programming-Collective-Intelligence_Reading
---

- PageRank
- Linear Algebra Done Right,3E

 
# Programming-Collective-Intelligence_by Toby Segaran

[*英文版官方*](http://pan.baidu.com/s/1ntKHRPB)
[*中文版PDF电子书免费下载地址*](http://pan.baidu.com/s/1ntKHRPB)


***
# 阅读记录

#### Chapter 2 Making recommendations
1. 相似性度量方法，or 机器学习中的距离度量 
	[机器学习算法 原理、实现与实践 —— 距离的度量](http://www.cnblogs.com/ronny/p/4080442.html)

	[漫谈：机器学习中距离和相似性度量方法](http://www.cnblogs.com/daniel-D/p/3244718.html)

	==目标： 从样本空间、行业知识以及计算效率的角度，理解不同距离度量方法的适用性和区别。==


2. 计算效率
3. 待定


***
#### Chapter 4 Searching and Ranking
#### 搜索和排名

- Ｇoogle ＰageRank 算法思想简述
-- 0. Ｒeference： 《数学之美》 by 吴军

-- 1. **ＰageRank的核心思想**
	在互联网上，如果一个网页被很多其他网页所链接，说明它受到普遍的承认和信赖，那么他的排名就高。举例，一个网页y的排名应该来自于所有指向这个网页的其他网页x<sub>1</sub>,x<sub>2</sub>,x<sub>3</sub>,...,x<sub>k</sub>的权重之和。至于x~i~的权重分别是多少，如何度量，及网页本身的网页排名。
	
-- 2. **迭代算法**
	“计算搜索结果的网页排名的过程中需要用到网页本身的排名，这不成了’先有鸡还是先有蛋‘的问题了吗？" 解决的办法是通过矩阵相乘的迭代，即先假设所有网页排名相同，作为初始值，算出哥哥网页的第一次迭代排名，然后根据第一次迭代排名算出第二次的排名，布林和佩奇二人从理论上证明了无论初始值如何选取，此算法总是能收敛到真实值，并不需要人工干预。 
	
-- 3.  **工程问题**
	互联网上网页的数量是巨大的，假定有十亿个网页，矩阵就有一百亿个元素。佩奇和布林利用稀疏矩阵计算的技巧，大大简化了计算量，实现了网页排名算法。
	
-- 4. **并行计算**
	2003年，Ｇoogle工程师Ｊeffrey Dean和Ｓanjay Ghemawat发明了并行计算工具ＭapReduce，实现ＰageRank的并行计算。
	
-- 5. **ＰageRank的计算方法**
--- 迭代方法，获得收敛结果；
--- 数学上，等效为平稳马尔可夫过程 (stationary Markov process)
---**tip** 迭代方法，数学上可以表示成算子的指数运算，即P<sub>n</sub>=H<sup>n</sup>P<sub>0</sub>


-- 6. **Learning from Clicks**
	==提高搜索结果的核心——利用用户点击查询结果的信息。
	构造ＡＮＮ==
	
-- 7. **更具体的讨论**
[PageRank算法--从原理到实现](http://www.cnblogs.com/rubinorth/p/5799848.html)
博文中附有较为专业的资料

	
-- 6. 怎么想到ＰageRank算法的？ 
	据《数学之美》中叙述，佩奇讲起他当年和布林是怎么想到网页排名算法的，他说：”当时我们觉得整个互联网就像一张大的图，每个网站就像一个节点，而每个网页的链接就像一个弧。我想，互联网可以用一个图或者矩阵描述，我也许可以用这个发现做篇博士论文。“	
	


