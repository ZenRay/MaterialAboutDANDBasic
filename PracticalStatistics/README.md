**目录**

[TOC]

## 说明
罗列出相关文件列表目录



## 课程材料

### 课程1 [选修]描述统计学-第一部分



### 课程12 假设检验

1. 12 假设检验的一般类型

   * [单样本 t 检验](https://www.cliffsnotes.com/study-guides/statistics/univariate-inferential-tests/one-sample-t-test)

     > 要求是：符合正态分布，而且 $\sigma$ 是未知；公式： $t=\frac{\hat{x}-\Delta}{\frac{s}{\sqrt{n}}}$ ，其中 $\Delta$ 表示的是已知的总体均值，可能用 $\mu$ 表示

   * [双样本 t 检验](http://www.itl.nist.gov/div898/handbook/eda/section3/eda353.htm)

     > 用于检验两个总体的均值是否相等；公式：1) $T = \frac{\bar{Y_{1}} - \bar{Y_{2}}} {s_{p}\sqrt{1/N_{1} + 1/N_{2}}}$;2)$s_{p}^{2} = \frac{(N_{1}-1){s^{2}_{1}} + (N_{2}-1){s^{2}_{2}}} {N_{1} + N_{2} - 2}$，表示联合方差计算公式

   * [配对 t 检验](./课程材料/配对t检验.pdf) 原始地址：[配对 t 检验](http://www.statstutor.ac.uk/resources/uploaded/paired-t-test.pdf)

     > 处理的问题类型：1）试验前后差异比较；2）同样主体下的两种不同试验方法的比较

   * [双样本 z 检验](https://onlinecourses.science.psu.edu/stat414/node/268)

     > 处理的是双总体中比例差异问题。公式：$Z=\frac{(\hat{p_1}-\hat{p_2})-(p_1-p_2)}{\sqrt{\hat{p}*(1-\hat{p})*(\frac{1}{n_1}+\frac{1}{n_2})}}$，其中合并比例 $\hat{p}=\frac{Y_1+Y_2}{n_1+n_2}$，公式中需要注意$p_1-p_2$ 的值可能是 $0$ ，也可能是其他值，这是需要根据试验判定，最好的可能是根据试验假设 $H_0$ 来判断该值

   * [单样本 z 检验](https://stattrek.com/statistics/dictionary.aspx?definition=one-sample%20z-test)

     > 被用于检验总体的参数的假设检验是否具有统计显著性差异


## [课程练习](./课程练习)

### 课程 11 置信区间

* [09-confidence-intervals](课程练习/09-confidence-intervals.zip) 本小节练习
* [09-data ](课程练习/09-data.zip) 本小节练习用数据

### 课程12 假设检验

* [10-data](课程练习/10-data.zip) 	本小节练习用数据
* [10-hypothesis-testing](课程练习/10-hypothesis-testing.zip) 本小节练习

### 课程 13 案例研究：A/B 测试

* [notebook-solutions](课程练习/notebook-solutions.zip) 本小节练习

### 课程 14 线性回归

* [12-data](课程练习/12-data.zip) 数据

  [12-regression](课程练习/12-regression.zip) 练习

## [项目材料](./项目材料/)

* [analyzeabtestresults](项目材料/analyzeabtestresults.zip) 项目材料文件