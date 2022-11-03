---
slug: /
sidebar_position: 1
---

# 概述

<div align="center">

<img alt="logo.svg" width="230" src="img/logo.svg" />

[![License](https://img.shields.io/badge/License-Commercial%20or%20SSPL-green?color=2fbf43?link=https://github.com/vkit-x/vkit/blob/master/LICENSE.txt)](https://github.com/vkit-x/vkit/blob/master/LICENSE.txt)
[![(Procedure) Test every hour](https://github.com/vkit-x/vkit/actions/workflows/procedure-test-every-hour.yaml/badge.svg)](https://github.com/vkit-x/vkit/actions/workflows/procedure-test-every-hour.yaml)

</div>

## 这是什么项目？

vkit（[GitHub 仓库](https://github.com/vkit-x/vkit)）聚焦于**计算机视觉、文档智能**领域，以对**数据质量极致追求**的态度，助力**研究员、算法工程师**，化繁为简，使不可能成为可能。

具体而言，目前 vkit 可以为用户提供以下 解决方案 ：

- 完善、通用的图片数据增强组件，适用于大多数场景的计算机视觉模型训练流程，详见 🏷️*[通用图片数据增强](/solution/data-augmentation)* 。
- 与众不同、高质量的文字检测合成数据，适用于 OCR、文档智能模型的预训练，详见 🏷️*[文字检测合成数据](/solution/text-detection)* 。


## 如何开始？

建议先阅读 🏷️*[快速开始](/quick-tour/quickstart)* 与 🏷️*[设计理念](/quick-tour/philosophy)* ，然后按需阅读 🏷️*[解决方案](/solution)* 与 🏷️*[教程](/tutorial)* 中的相关章节。如果在过程中遇到问题，可以按照 🏷️*[参与指引](/quick-tour/参与指引)* 联系我们。

## 来点眼前一亮的东西？

### 解决方案：通用图片数据增强

作为深度学习的最佳实践之一，[数据增强](https://en.wikipedia.org/wiki/Data_augmentation)方法被广泛应用在计算机视觉领域学术研究、工业落地的模型训练过程。vkit 内置了丰富的 🏷️*[通用图片数据增强](/solution/data-augmentation)* 策略，包括**仿射变换、MLS、相机模型成像、色彩、模糊度、噪点、环境效果、条纹**等不同维度的多种策略实现，帮助用户**高效、高质量**地扩充训练数据集，从而增强模型的泛化性与最终效果。

无心插柳柳成荫，作为项目的副产物，vkit 在不经意间封装了一个**易用的图片编辑解决方案**，用户仅需要写几行代码即可完成简单的图片编辑操作。详见 🏷️*[简易图片编辑](/solution/image-editing)* 。

以下是 vkit 数据增强解决方案的可视化效果展示。

原始图片：

<div align="center">

<img alt="logo.svg" width="250" src="img-docs/quick-tour/introduction/Rooster-resized.jpg" />

</div>

数据增强后的效果图：

<div align="center">

<img alt="logo.svg" width="648" src="img-docs/quick-tour/introduction/all-in-one-optim.gif" />

</div>
