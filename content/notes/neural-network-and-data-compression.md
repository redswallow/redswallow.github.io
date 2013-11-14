title: 神经网络与数据压缩
slug: neural-network-and-data-compression
date: 2013-10-19
tags: PCA, 神经网络, 数据压缩

神经网络除了用于Regreesion和Classification，还可以与用于数据压缩Data Compression。自联想神经网络Auto-Associative Neural Network是三层BP网络，它的特点是输出是对输入的一种重构，即输出等于输入或者允许输入输出有一定的误差存在。如果中间层Hidden Layer节点少于输入层Input Layer，中间层可以用更少节点表示输入层的数据同时可以在输出层重构出输入层数据，这就是数据压缩和解压的过程。

从另一个角度来看，中间层提取出数据中最重要的特征，用更少维度表示输入数据。如果我们在网络中不使用sigmoid函数，而使用线性函数，这就是主成分分析PCA模型。

在深度学习中，上述结构被称作自编码神经网络Autoencoder Neural Network。
