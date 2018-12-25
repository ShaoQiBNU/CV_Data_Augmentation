Data Augmentation using Random Image Cropping and Matching for Deep CNNs 论文解读
================================================================================

# 一. 背景

> 论文提出了一种基于随机图像裁剪和修补的图像预处理方法 RICAP，随机裁剪四个图像并对其进行修补以创建新的训练图像。该方法非常简单实用，把几张图拼在一起，然后 label 就是这几张图类别占图片大小的比率。

# 二. RICAP

## (一) 简介

> RICAP的具体过程如图所示，具体步骤如下：

img1

```
1. 随机选择4张影像

2. 对4张影像进行裁剪

3. 裁剪后的影像拼接在一起
```

## (二) 裁剪

> 裁剪具体过程如图所示，具体步骤如下：

img2

## (三) label smoothing

> Label smoothing的具体步骤如下：

Img3

## (四) 参数确定

> 裁剪和label smoothing过程均涉及到参数<a href="https://www.codecogs.com/eqnedit.php?latex=\beta" target="_blank"><img src="https://latex.codecogs.com/gif.latex?\beta" title="\beta" /></a>的确定，关于该参数论文的讨论如下：

Img4

# 三. 结果

> 论文将此方法在CIFAR-10、CIFAR-100和ImageNet数据集上进行了测试，对结果进行了比较，对比结果如下：

Img5
