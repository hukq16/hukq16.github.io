---
categories:
- 因果推断
date: '2022-01-24T04:18:00.000Z'
description: 介绍格兰杰因果及其各种变体
image: front_cover_b07d8ce2-d762-41a4-8e93-c19e50beee36.jpg
showToc: true
tags:
- 因果推断
- 格兰杰因果
- 时间序列
title: 格兰杰因果

---



# Granger因果指数(GCI)

由诺贝尔奖得主Granger提出的一种”因果关系”分析模型,在金融,自然,医学领域得到普遍使用.

基本思想是:若采用时间序列X和Y的历史信息对Y进行预测, 优于仅采用Y的历史信息对Y进行预测的结果, 即时间序列X有助于解释时间序列Y的未来变化趋势, 那么时间序列X是时间序列Y的**Granger原因**.(注意:并不能说明确实存在因果关系)

该模型通过随机过程的线性回归模型实现.其分析的前提是<u>**时间序列为平稳序列**</u>,否则可能出现虚假因果.

考虑以下两个向量自回归(VAR)模型:

$$
Y_{t+1} = \sum^{m-1}_{j=0}{\alpha_{j} Y_{t-j}} + \varepsilon_{Y,t+1} 
$$

$$ Y_{t+1} = \sum_{j = 0}^{m-1}{a_j X_{t-j}} + \sum_{j = 0}^{m - 1}{b_j Y_{t - j}} + \varepsilon _{Y|X,t+1} $$

其中，$ \alpha_j,a_j,b_j $为模型的系数,m为模型的阶数,$ \varepsilon_{Y,t+1},\varepsilon _{Y|X,t+1} $为在t+1时刻,模型的残差.一般而言,模型的阶数根据先验知识指定,也可通过学习的方式得到;模型的系数由训练得到,使得模型的残差最小.

在模型构建完毕后,根据预测的结果,可通过比较该VAR模型残差的方差大小,判断$ X \to Y $是否存在Granger因果关系.其Granger因果指数(GCI)可定义为:

$$ GCI_{X \to Y} = ln{\frac{var(\varepsilon_Y)}{var(\varepsilon_{Y|X})}}  $$

如果满足$ var(\varepsilon_{Y|X}) < var(\varepsilon_{Y}) $,即使用X和Y对Y变量进行联合预测(回归)的残差比Y变量自回归的残差要小,即使用X和Y对Y变量进行联合预测(回归)的效果比Y变量自回归的效果要好.那么表示$ X \to Y $存在**统计意义**下的Granger因果关系,预测的效果越好,因果关系越强. 

### 缺点

1. 建立在线性模型的基础上,无法直接应用到非线性系统

1. 仅对两个变量进行分析

1. 要求时间序列具有平稳性.

# 条件Granger因果指数(CGCI)

考虑到多变量的影响,

<br/>

<br/>

<br/>

<br/>

[child_database is not supported]

