---
layout: post
read_time: true
show_date: true
title: 【阅读】Recent progress and trends in predictive visual analytics
date: 2021-08-16 
description: Single neuron perceptron that classifies elements learning quite quickly.
img: posts/20210125/Perceptron.jpg
tags: [visual analytics, predict, neural networks]
author: Armando Maynez
github: amaynez/Perceptron/
mathjax: yes
---

![论文结构思维导图](./images/Untitled.png)

评估相似样本中可能发生类似的趋势、模式或行为的可能性

视觉分析：结合自动分析，以人为中心

![enter description here](./images/Untitled-2.png)
---

## 数据预处理Data pre-processing

关键步骤：确保数据的完整性和准确性

可视化可以帮助人们识别出一些明显的问题数据，比如预测给定社区犯罪发生的可能性，根据 以往的犯罪数据，将犯罪地点进行可视化，在地图中可以明显发现一些异常错误数据，如0维度和0经度的地点。

步骤：

### 数据清洗

数据量的大量增长会导致处理数据的成本增加。目前没有一种方法能够适合所有数据清洗方法。缺少值、拼写错误、缩写词等都是现存的问题。数据清洗的目的就是去尽可能识别并消除异常。但目前有六种主要的数据形式（表格、时间序列、时空等），但是对于每一种数据，寻找错误可能要求一种或者多种可视化方法。比如时间序列数据，可能存在日期不匹配的情况（12-1-2012和12月1日，2012）。

### 数据转换

一些研究提出通过自动数据重新格式化、提取、转换等方式将一个数据元素转换为另一个数据元素，从而可以识别出一个可以自动查找和纠正脏数据的规则。现有的研究主要致力于文本的提取和转换，但这些不能处理数据缺失或者错误输入的问题。

### 数据集成和融合

基于阶段的融合：将松散的数据耦合/集成

基于特征级别的融合：数据特征跨数据集提取和合并

基于语义的融合：在融合阶段使用关于特征的先验知识

## 特征选择和生成Feature selection and generation

选择合适的特征（数据属性）去构建模型，其中特征要捕获数据中最具代表性的方面。如果没有合适的选择，冗余和非描述性特征会导致意料之外的训练结果和差劲的预测。

特征选择尝试去选择特征的最小子集：不显著降低分类的准确性；必须匹配（尽可能接近）所有给定特征的原始分布。

理想的特征选择将搜索所有特征的子集。

删除冗余特征以方便用户选择显著特征。

## 模型训练、选择和验证Model training, selection and validation

在特征选择，一项关键任务是识别模型训练中应使用的冗余最少的最显著特征。

模型验证的两个关键策略：模型（参数）的比较；识别有问题的特征和样本。