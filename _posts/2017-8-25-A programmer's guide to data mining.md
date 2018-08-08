---
key: 20170825
title: '读书笔记: A Programmers Guide to Data Mining'
tags: 读书笔记 数据挖掘
---
## Chapter 1 Introduction
![](http://guidetodatamining.com/img/mozi.png)
[A Programmer's Guide to Data Mining](http://guidetodatamining.com/)
数据分析基本知识，每个程序员最好了解。

## Chapter 2: Get Started with Recommendation Systems
### 曼哈顿距离 Manhattan Distance
```mathjax
Manhattan(x,y)=\sum_{i=1}^n|x_i-y_i|
```
### 欧几里得距离 Euclidean Distance
```mathjax
Euclidean(x,y)=(\sum_{i=1}^n{|x_i-y_i|}^2)^{1\over2}
```

### 泛化 A generalization
```mathjax
d(x,y)=(\sum_{i=1}^n{|x_i-y_i|}^r)^{1\over r}
```
如果数据结构是高密度类型（数据整齐，很少缺失或0值），且数值本身的意义重大，那么则使用曼哈顿或欧几里德距离。
If your data is dense
(almost all attributes have non- zero values) and the magnitude of the attribute values is important, use distance measures such as Euclidean or
Manhattan.

**r值越大，灵敏度越高：任何一个维度的差异对整体结果的影响随着r的增加而增加。**
**The greater the r, the more a large difference in one dimension will influence the total difference.**

因此调高r值可以更精确的计算距离，当然r越大计算的代价越高。

### 基于用户的相关性分析: 皮尔松相关系数 Pearson Correlation Coefficient
皮尔松相关系数 Pearson Correlation Coefficient，系数的值在0~1之间，0表示不相关，1表示行为完全一致。
```mathjax
r={ { {\sum_{i=1}^nx_iy_i} - {{ {\sum_{i=1}^nx_i}{\sum_{i=1}^ny_i}} \over {n} } } \over { \sqrt{ {\sum_{i=1}^n{x_i}^2} - {(\sum_{i=1}^n{x_i})^2 \over n} }  \sqrt{ {\sum_{i=1}^n{y_i}^2} - {(\sum_{i=1}^n{y_i})^2 \over n} }  }  }
```
如果数据结构等级膨胀类型，则使用皮尔松系数计算相关性。
If the data is subject to grade-inflation (different users may be using different scales) use Pearson.
```不同的人评价或打分的基数不一样，使用皮尔松系数可以去除基数差别带来的影响。```

### 余弦相似性 Cosine Similarity
余弦相似性分析在[文本挖掘](https://zh.wikipedia.org/wiki/文本挖掘)与[协同过滤](https://zh.wikipedia.org/wiki/協同過濾)领域使用非常普遍。
I would like to present one last formula, which is very popular in text mining but also used in collaborative filtering—cosine similarity.

余弦相似性适用于稀疏的数据结构。
If the data is sparse consider using Cosine Similarity.

余弦相似性函数定义:
```mathjax
cos(x,y)={ {{\vec x}{\vec y}}\over {||x||*||y||} }
```

公式中的分子表示向量x与y的[数量积](https://zh.wikipedia.org/wiki/数量积)；分母||x||与||y||分别表示向量x与y的长度。

公式可展开为：
```mathjax
cos(x,y)={ {\sum_{i=1}^nx_iy_i} \over { \sqrt{\sum_{i=1}^n{{x_i}^2}}\sqrt{\sum_{i=1}^n{{y_i}^2}} } }
```

### K-nearest neighbor

## Chapter 3: Implicit ratings and item-based filtering
## Chapter 4: Classification
## Chapter 5: Further Explorations in Classification
## Chapter 6: Naïve Bayes
## Chapter 7: Naïve Bayes and unstructured text
## Chapter 8: Clustering