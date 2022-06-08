# 卷积神经网络基础


图像分类：

LeNet

AlexNet

VggNet

GoogLeNet

ResNet

目标检测：

Faster R-CNN

SSD

Yolo　ｖ３

图像分割：



卷积神经网络基础：

卷积神经网络

全连接层：　　BP

卷积层：１，局部感知机制

​				２，权值共享　

​	卷积越界的情况：输入图片大小W＊Ｗ　，filter大小F＊F，步长S，padding的像素P

​	经过卷积后矩阵尺寸大小为：

​	N＝（W－F＋２P）／Ｓ＋１

池化层：Max Pooling下采样层，Average Pooling下采样层

​	目的：对特征图进行稀疏处理，减少数据运算量。

​	特点：没有训练参数；只改变特征矩阵的ｗ和ｈ，不改变channel；一般池化核大小和步长相同。

反向传播：

​	误差的计算，　　

​	误差的反向传播



在本文中我们研究了新类发现的问题（NCD）。NCD 旨在利用包含不同但相 关类的标记集的先验知识，在未标记集中推断新的对象类别。与传统的半监督学 习相比，这是一个更现实、更具挑战性的任务。现有的方法大多是通过考虑多个目 标函数来解决这个问题，通常分别涉及标记样本和未标记样本的特殊损失项，并 且通常需要辅助正则化项。在本文中，我们在传统的方案的基础上，引入了一个 统一的目标函数（UNO）来发现新的类别，目的是支持监督和非监督学习之间的 协同。使用多视图自标记策略生成伪标签，这些伪标签可以与真值标签进行均匀 处理。这就构造了一个单一的分类目标，既适用于已知的类别，也适用于未知的 类别。 

本文还使用了更强大的数据增广策略以及 multi-crop 的方法，通过更长时间的训练来提高它的表现。尽管它很简单，但 UNO 在几个基准上都以显著优势超越了 最先进的水平。

In this paper , we study the problem of Novel Class Discovery (NCD). NCD aims at inferring novel object categories in an unlabeled set by leveraging from prior knowledge of a labeled set containing different, but related classes. This is a more realistic and challenging setting than conventional semi-supervised learning. Existing approaches tackle this problem by considering multiple objective functions, usually involving specialized loss terms for the labeled and the unlabeled samples respectively, and often requiring auxiliary regularization terms. In this paper we depart from this traditional scheme and introduce a UNified Objective function (UNO) for discovering novel classes, with the explicit purpose of favoring synergy between supervised and unsupervised learning. Using a multi-view self-labeling strategy, we generate pseudo-labels that can be treated homogeneously with ground truth labels. This leads to a single classification objective operating on both known and unknown classes.

We also use a more powerful data augmentation strategy as well as a Multi-crop approach to improve its performance by training for a longer time. Despite its simplicity, UNO outperforms the state of the art by a significant margin on several benchmarks. This thesis conducts experiments on two public data sets, CIFAR-100 and ImageNet, to verify the effectiveness of the proposed method, discuss and analyze the experimental results.

从标记数据学习一直是深度学习领域中一个广泛研究的课题，但大规模注释数据成本昂贵，且在特定领域（如医疗）标签数据不易获得。为此本文研究了新类发现（Novel Class Discovery ）的问题。利用包含不同但相关类的标记集的先验知识，在未标记集中推断新的对象类别的方法称为新类发现。现有的方法大多需要多种损失来驱动模型的训练，并且需要重复进行自监督预训练阶段，成本非常高。

针对上述问题，本文引入了一个统一的目标函数来发现新的类别，目的是支持监督和非监督学习之间的协同。使用多视图自标记策略生成伪标签，这些伪标签可以与真实标签进行均匀处理。这就构造了一个单一的分类目标，既适用于已知的类别，也适用于未知的 类别。本文还使用了更强大的数据增广策略以及 Multi-crop 的方法，通过更长时间的训练来提高它的表现。本文在 CIFAR-100 和 ImageNet 等公开数据集上进行实验测试，验 证了方法的有效性，并对实验结果进行讨论分析。

Learning from labeled data has been a widely studied topic in the field of deep learning, but large-scale annotated data is expensive, and labeled data in specific domains (such as medical) are not readily available.In this paper, we study the problem of Novel Class Discovery (NCD). NCD aims at inferring novel object categories in an unlabeled set by leveraging from prior knowledge of a labeled set containing different, but related classes. Most of the existing methods require multiple losses to drive the training of models, and require repeated self-supervised pre-training, which is very expensive.

For the above problems, this thesis introduce a UNified Objective function (UNO) for discovering novel classes, with the explicit purpose of favoring synergy between supervised and unsupervised learning. Using a multi-view self-labeling strategy, we generate pseudo-labels that can be treated homogeneously with ground truth labels. This leads to a single classification objective operating on both known and unknown classes. We also use a more powerful data augmentation strategy as well as a Multi-crop approach to improve its performance by training for a longer time. This thesis conducts experiments on two public data sets, CIFAR-100 and ImageNet, to verify the effectiveness of the proposed method, discuss and analyze the experimental results.








