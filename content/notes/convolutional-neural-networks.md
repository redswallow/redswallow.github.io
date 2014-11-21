title: 卷积神经网络
slug: convolutional-neural-networks
date: 2014-04-26
tags: deep learning, CNN

卷积神经网络(Convolutional Neural Networks：CNN)是人工神经网络(ANN)的一种，是深度学习的一种学习算法。它在图像识别和分类、自然语言处理广告系统中都有应用。

有意思是，卷积神经网络的提出其实就是来自于生物视觉模型。1981年的诺贝尔医学奖，颁发给了David Hubel、Torsten Wiesel。他们的工作给人们呈现了视觉系统是如何将来自外界的视觉信号传递到视皮层，并通过一系列处理过程（包括边界检测、运动检测、立体深度检测和颜色检测），最后在大脑中构建出一幅视觉图像。这个发现激发了人们对于神经系统的进一步思考，神经-中枢-大脑的工作过程，或许是一个不断迭代、不断抽象的过程。从原始信号摄入开始（瞳孔摄入像素Pixels），首先进行初步处理（大脑皮层某些细胞发现边缘和方向），抽象（大脑判定眼前的物体的形状是圆形的），然后进一步抽象（大脑进一步判定该物体是只气球）。

![convolutional deep belief network](http://pic.yupoo.com/redswallow_v/DIrrc7nd/12P76C.png)

六十年代的生理学的发现，促成了计算机人工智能在四十年后的突破性发展。1989年，[Yann LeCun](http://yann.lecun.com/) (现纽约大学教授，FacebookAI研究室主任) 提出了卷积神经网络，这是第一个真正成功训练多层网络结构的学习算法，但在当时的计算能力下效果欠佳。直到2006年，[Geoffrey Hinton](https://www.cs.toronto.edu/~hinton/)提出基于深信度网（Deep Belief Net）和限制波尔兹曼机（Restricted Boltzmann Machine）的学习算法，重新点燃了人工智能领域对于神经网络的热情。

卷积神经网络现在计算机视觉领域表现出众。[ImageNet Classification with Deep Convolutional Neural Networks](http://papers.nips.cc/paper/4824-imagenet-classification-with-deep-convolutional-neural-networks)，这篇发表于NIPS2012的文章，是Hinton与其学生Matthew Zeiler为了回应别人对于Deep Learning的质疑而将CNN结合GPU并行技术用于[Imagenet Challenge](http://image-net.org/)（图像识别目前最大的数据库，被誉为计算机视觉圣杯），最终取得了非常惊人的结果。最终取得了非常惊人的结果。他们的算法在2012年取得世界最好结果，使分类错误率从26.2%下降到16%。2013年Matthew Zeiler的算法继续将错误率下降到11.2%。[Matthew Zeiler](http://www.matthewzeiler.com/)还创立了[Clarifai](http://www.clarifai.com/)，让我们可以有机会使用他们的图像识别算法对图片标注分类或图像搜索。

![imageNet classification with CNN](http://pic.yupoo.com/redswallow_v/DIru6ltO/kMvRI.jpg)

在月初Kaggle结束的[Galaxy Zoo challenge](http://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge)中，参赛者要对星系图像进行分类(Spiral/Elliptical, Merging/Not merging, Clockwise/Anti-clockwise)，获胜的算法也是使用了卷积神经网络。Sander Dieleman已放出了代码和详尽的文档: 
[My solution for the Galaxy Zoo challenge](
http://benanne.github.io/2014/04/05/galaxy-zoo.html)

2014年3月，Facebook刚刚公布了他们在CVPR2014的文章：[DeepFace: Closing the Gap to Human-Level Performance in Face Verification](https://www.facebook.com/publications/546316888800776/)。他们用四百万人脸图片训练了一个九层的卷积神经网络来获得脸部特征，神经网络处理的参数高达1.2亿。他们在著名的公共测试数据集[LFW](http://vis-www.cs.umass.edu/lfw/results.html
)（labeled face in the wild，1v1地判断是否两个照片是一个人）上达到了97.25%的正确率。这个数字已经基本接近人眼的辨识水平。
北京[Face++](http://www.faceplusplus.com/)团队的算法达到97.27%的正确率，在美图秀秀中就有应用，他们的主页提供了API、demo展示和论文。现在的最新进展是，香港中文大学基于 Fisher Discriminant Analysis的算法将Face Verification正确率提高到98.52%，超过了人类水平（97.53%）

![System overview in Face++ paper in ICCV2013](http://pic.yupoo.com/redswallow_v/DIrIkyIl/14MIOn.jpg)

除了计算机视觉领域，卷积神经网络还可以用于人工智能。Hinton的另外一个学生创立了DeepMind（已被Google招聘式收购），他们使用深度学习（CNN）结合强化学习（Reinforcement Learning），在Stella模拟机上让机器自己玩了7个Atari 2600的游戏，结果不仅战胜了其他机器人，甚至在其中3个游戏中超越了人类游戏专家。很有意思，具体可以见InfoQ的[看DeepMind如何用Reinforcement learning玩游戏](http://www.infoq.com/cn/articles/atari-reinforcement-learning)，以及原始论文[Playing Atari with Deep Reinforcement Learning](http://arxiv.org/abs/1312.5602)