# 打卡：简化版笔记
从线性回归，Softmax回归与分类模型、多层感知机、文本预处理到循环神经网络，有很多需要深入研究的地方  

用pytorch实现，首先有问题查找官方torch说明文档：  

https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html  

目前对tensorflow的了解还是有限，无法具体具体比较tensor和torch使用区别，期待后续学习


## 线性回归
1模型：  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/线性回归.png)

2损失函数：  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/损失函数.png)  

3优化函数  

![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/优化.png)

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
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/交叉熵损失函数.png)。

3两种实现方法：  

（之后会做成py文件放到库里）

## 多层感知机：MLP  
![image](https://github.com/yilin1168/learn_deeplearning/blob/master/images/多层感知机表达公式.png)。



##过拟合及欠拟合  



###模型误差  


训练误差（training error）指模型在训练数据集上表现出的误差；泛化误差指模型在任意一个测试数据样本上表现出的误差的期望，并常常通过测试数据集上的误差来近似。计算训练误差和泛化误差可以使用之前介绍过的损失函数，例如线性回归用到的平方损失函数和softmax回归用到的交叉熵损失函数。机器学习模型应关注降低泛化误差。  

训练误差（training error）指模型在训练数据集上表现出的误差；泛化误差指模型在任意一个测试数据样本上表现出的误差的期望，并常常通过测试数据集上的误差来近似。计算训练误差和泛化误差可以使用之前介绍过的损失函数，例如线性回归用到的平方损失函数和softmax回归用到的交叉熵损失函数。机器学习模型应关注降低泛化误差。  

###模型选择  


验证数据集: 从严格意义上讲，测试集只能在所有超参数和模型参数选定后使用一次。不可以使用测试数据选择模型，如调参。由于无法从训练误差估计泛化误差，因此也不应只依赖训练数据选择模型。鉴于此，我们预留一部分在训练数据集和测试数据集以外的数据来进行模型选择。这部分数据被称为验证数据集，简称验证集（validation set）。例如，我们可以从给定的训练集中随机选取一小部分作为验证集，而将剩余部分作为真正的训练集。  

K折交叉验证: 由于验证数据集不参与模型训练，当训练数据不够用时，预留大量的验证数据显得太奢侈。一种改善的方法是K折交叉验证（K-fold cross-validation）。所谓K折交叉验证，就是将数据集等比例划分成K份，以其中的一份作为测试数据，其他的K-1份数据作为训练数据。然后，这样算是一次实验，而K折交叉验证只有实验K次才算完成完整的一次，也就是说交叉验证实际是把实验重复做了K次，每次实验都是从K个部分选取一份不同的数据部分作为测试数据（保证K个部分的数据都分别做过测试数据），剩下的K-1个当作训练数据，最后把得到的K个实验结果进行平分。



