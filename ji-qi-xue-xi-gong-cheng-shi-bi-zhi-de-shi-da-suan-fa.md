# 机器学习工程师必知的十大算法

毫无疑问，机器学习/人工智能的子领域在过去几年越来越受欢迎。目前大数据在科技行业已经炙手可热，而基于大量数据来进行预测或者得出建议的机器学习无疑是非常强大的。一些最常见的机器学习例子，比如Netflix的算法可以根据你以前看过的电影来进行电影推荐，而Amazon的算法则可以根据你以前买过的书来推荐书籍。

所以如果你想了解更多有关机器学习的内容，那么你该如何入门？对于我来说，我的入门课程是我在哥本哈根出国留学时参加的人工智能课。当时我的讲师是丹麦技术大学（Technical University of Denmark）的应用数学和计算机科学的全职教授，他的研究方向是逻辑与人工智能，侧重于使用逻辑学来对人性化的规划、推理和解决问题进行建模。这个课程包括对理论/核心概念的讨论和自己动手解决问题。我们使用的教材是AI经典之一：Peter Norvig的Artificial Intelligence—A Modern Approach（中文译本：[《人工智能：一种现代的方法》](https://book.douban.com/subject/6730363/)），这本书主要讲了智能体、搜索解决问题、对抗搜索、概率论、多智能体系统、社会AI和AI的哲学/伦理/未来等等。在课程结束时，我们三个人的团队实现了一个简单的编程项目，也就是基于搜索的智能体解决虚拟环境中的运输任务问题。

在那门课程上我已经学到了很多知识，并决定继续学习相关的课题。在过去的几个星期里，我在旧金山参加了多次相关的技术讲座，涉及到深度学习、神经网络和数据结构，并且参加了一个有很多该领域的知名专家学者参加的机器学习会议。最重要的是，我在6月初参加了Udacity上的[Intro to Machine Learning（机器学习入门）](https://cn.udacity.com/course/intro-to-machine-learning--ud120)在线课程，前几天才完成。在这篇文章中，我想分享一下我从课程中学到的一些最常用的机器学习算法。

机器学习算法可以分为三大类：监督学习、无监督学习和强化学习。监督学习可用于一个特定的数据集（训练集）具有某一属性（标签），但是其他数据没有标签或者需要预测标签的情况。无监督学习可用于给定的没有标签的数据集（数据不是预分配好的），目的就是要找出数据间的潜在关系。强化学习位于这两者之间，每次预测都有一定形式的反馈，但是没有精确的标签或者错误信息。因为这是一个介绍课程，我没有学习过强化学习的相关内容，但是我希望以下10个关于监督学习和无监督学习的算法足以让你感兴趣。

## 监督学习

### 1.决策树（Decision Trees）

决策树是一个决策支持工具，它使用树形图或者决策模型以及可能性序列，包括偶然事件的结果、资源成本和效用。下图是其基本原理：

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/0.jpg)

从业务决策的角度来看，决策树是人们必须了解的最少的是/否问题，这样才能评估大多数时候做出正确决策的概率。作为一种方法，它允许你以结构化和系统化的方式来解决问题，从而得出合乎逻辑的结论。

### 2.朴素贝叶斯分类\(Naive Bayesian classification\)

朴素贝叶斯分类器是一类简单的概率分类器，它基于贝叶斯定理和特征间的强大的（朴素的）独立假设。图中是贝叶斯公式，其中P（A\|B）是后验概率，P（B\|A）是似然，P（A）是类先验概率，P（B）是预测先验概率。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/1.jpg)

一些应用例子:

* 判断垃圾邮件
* 对新闻的类别进行分类，比如科技、政治、运动
* 判断文本表达的感情是积极的还是消极的
* 人脸识别

### 3.最小二乘法（Ordinary Least Squares Regression）

如果你懂统计学的话，你可能以前听说过线性回归。最小二乘法是一种计算线性回归的方法。你可以将线性回归看做通过一组点来拟合一条直线。实现这个有很多种方法，“最小二乘法”就像这样：你可以画一条直线，然后对于每一个数据点，计算每个点到直线的垂直距离，然后把它们加起来，那么最后得到的拟合直线就是距离和尽可能小的直线。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/2.jpg)

线性指的是你用来拟合数据的模型，而最小二乘法指的是你最小化的误差度量。

### 4.逻辑回归\(Logistic Regression\)

逻辑回归是一个强大的统计学方法，它可以用一个或多个解释变量来表示一个二项式结果。它通过使用逻辑函数来估计概率，从而衡量类别依赖变量和一个或多个独立变量之间的关系，后者服从累计逻辑分布。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/3.jpg)

总的来说，逻辑回归可以用于以下几个真实应用场景：

* 信用评分
* 计算营销活动的成功率
* 预测某个产品的收入
* 特定的某一天是否会发生地震

### 5.支持向量机（Support Vector Machine，SVM）

SVM是二进制分类算法。给定N维坐标下两种类型的点，SVM生成（N-1）维的超平面来将这些点分成两组。假设你在平面上有两种类型的可以线性分离的点，SVM将找到一条直线，将这些点分成两种类型，并且这条直线尽可能远离所有这些点。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/4.jpg)

从规模上看，使用SVM（经过适当的修改）解决的一些最大的问题包括显示广告、人类剪切位点识别（human splice site recognition）、基于图像的性别检测，大规模图像分类……

### 6.集成方法（Ensemble methods）

集成方法是学习算法，它通过构建一组分类器，然后通过它们的预测结果进行加权投票来对新的数据点进行分类。原始的集成方法是贝叶斯平均，但是最近的算法包括纠错输出编码、Bagging和Boosting。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/5.jpg)

那么集成方法如何工作？并且为什么它们要优于单个模型？

* 它们平均了单个模型的偏差：如果你将民主党的民意调查和共和党的民意调查在一起平均化，那么你将得到一个均衡的结果，不偏向任何一方。
* 它们减少了方差：一组模型的总体意见比其中任何一个模型的单一意见更加统一。在金融领域，这就是所谓的多元化，有许多股票的组合比一个单独的股票的不确定性更少，这也为什么你的模型在数据多的情况下会更好的原因。
* 它们不太可能过拟合：如果你有单个的模型没有过拟合，那么把这些模型的预测简单结合起来（平均、加权平均、逻辑回归），那么最后得到的模型也不会过拟合。

## 无监督学习

### 7.聚类算法（Clustering Algorithms）

聚类是将一系列对象分组的任务，目标是使相同组（集群）中的对象之间比其他组的对象更相似。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/6.jpg)

每一种聚类算法都不相同，下面是一些例子：

* 基于质心的算法
* 基于连接的算法
* 基于密度的算法
* 概率
* 降维
* 神经网络/深度学习

### 8.主成分分析（Principal Component Analysis，PCA）

PCA是一个统计学过程，它通过使用正交变换将一组可能存在相关性的变量的观测值转换为一组线性不相关的变量的值，转换后的变量就是所谓的主分量。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/7.jpg)

PCA的一些应用包括压缩、简化数据便于学习、可视化等。请注意，领域知识在选择是否继续使用PCA时非常重要。 数据嘈杂的情况（PCA的所有成分具有很高的方差）并不适用。

### 9.奇异值分解（Singular Value Decomposition，SVD）

在线性代数中，SVD是复杂矩阵的因式分解。对于给定的m \* n矩阵M，存在分解使得M=UΣV，其中U和V是酉矩阵，Σ是对角矩阵。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/8.jpg)

实际上，PCA是SVD的一个简单应用。在计算机视觉中，第一个人脸识别算法使用PCA和SVD来将面部表示为“特征面”的线性组合，进行降维，然后通过简单的方法将面部匹配到身份，虽然现代方法更复杂，但很多方面仍然依赖于类似的技术。

### 10.独立成分分析（Independent Component Analysis，ICA）

ICA是一种统计技术，主要用于揭示随机变量、测量值或信号集中的隐藏因素。ICA对观测到的多变量数据定义了一个生成模型，这通常是作为样本的一个大的数据库。在模型中，假设数据变量由一些未知的潜在变量线性混合，混合方式也是未知的。潜在变量被假定为非高斯分布并且相互独立，它们被称为观测数据的独立分量。

![](http://cdn.infoqstatic.com/statics_s2_20170919-0429u3/resource/articles/10-algorithms-machine-learning-engineers-need-to-know/zh/resources/9.jpg)

ICA与PCA有关，但是当这些经典方法完全失效时，它是一种更强大的技术，能够找出源的潜在因素。 其应用包括数字图像、文档数据库、经济指标和心理测量。

现在运用你对这些算法的理解去创造机器学习应用，为世界各地的人们带来更好的体验吧。

**查看英文原文：**[**The 10 Algorithms Machine Learning Engineers Need to Know**](http://www.kdnuggets.com/2016/08/10-algorithms-machine-learning-engineers.html/2)

