title: 压缩感知
slug: what-is-compressed-sensing
date: 2013-06-27
tags: 数据压缩, compressed sensing

压缩感知问题源自稀疏表示问题，两者的本质都是要在一定的约束条件下求得欠定方程的最稀疏解。Donoho在这个领域功不可没，也是压缩感知研究领域具有奠基性工作的人物。压缩感知的发现是个传说，2004年加州理工学院教授（现在在斯坦福）的Emmanuel Candes，Donoho的学生，在研究Shepp-Logan Phantom图像，这是医学图像处理领域用来进行仿真测试的标准模拟图像。Candes检查的图像质量非常差，充满了噪声，他想到一种名叫L1-minimization的数学算法能去除掉噪声条纹，结果算法真的起作用了，而且他发现在图像变干净的同时，图像的细节出人意料得完美，简直就像变魔术一样。

Emmanuel Candes后来向加州大学洛杉矶分校的同事陶哲轩介绍了自己的发现，陶哲轩是世界上搞调和分析的顶尖高手之一，于是陶哲轩、Emmanuel Candes和Donoho神牛们完善了理论，联手挖出了Compressed Sensing的大坑。
