---
categories:
- 因果推断
date: '2022-01-24T05:00:00.000Z'
description: 介绍了结构因果模型的相关理论
image: front_cover_b07d8ce2-d762-41a4-8e93-c19e50beee36.jpg
showToc: true
tags:
- SCM
- 因果推断
title: 结构因果模型SCM

---



## 定义

设U为外生变量的集合。外生变量属于模型外部，不必解释他们变化的原因。

设V为内生变量的集合，模型中每一个内生变量都至少是一个外生变量的后代。

外生变量不是任何其他变量的后代，在图中表现为一个根节点。

定义函数$ f $

$$ f = \{f_{X}:W_{X} \to X | X \in V\} $$

其中，$ W_{X} \subseteq (U \cup V)-\{X\} $，即函数$ f $根据模型其他变量的值给变量X赋值。

<br/>

<br/>

<br/>

<br/>

<br/>

如果知道每个外生变量的值，那么利用函数$ f_x \in f $，就能完全确定内生变量的值

[child_page is not supported]

