# 打卡：简化版笔记
从线性回归，Softmax回归与分类模型、多层感知机、文本预处理到循环神经网络，有很多需要深入研究的地方  

用pytorch实现，首先有问题查找官方torch说明文档：  

https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html  

目前对tensorflow的了解还是有限，无法具体具体比较tensor和torch使用区别，期待后续学习


## 线性回归
1模型：  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/线性回归.png）。

2损失函数：  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/损失函数.png）  

3优化函数  

![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/优化.png）  

4矢量计算  

-向量相加的一种方法是，将这两个向量按元素逐一做标量加法。  

-向量相加的另一种方法是，将这两个向量直接做矢量加法。这种方法所用时长小于第一种  

5两种实现方法  

-从零手动实现  

-pytorch实现  

（之后会做成py文件放到库里，更改数据源）

## softmax和分类模型
1分类问题  

2交叉熵损失函数：  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/交叉熵损失函数.png）
3两种实现方法：  

（之后会做成py文件放到库里）

## 多层感知机：MLP  

