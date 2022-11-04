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

目前，vkit 可以为用户提供以下解决方案：

- 完善、通用的图片数据增强组件，适用于大多数场景的计算机视觉模型训练流程，详见 [通用图片数据增强](/solution/data-augmentation)🏷️ 。
- 与众不同、高质量的文字检测合成数据，适用于 OCR、文档智能模型的预训练，详见 [文字检测合成数据](/solution/text-detection)🏷️ 。

此外，无心插柳柳成荫，vkit 在不经意间封装了一个**易用、可编程的图片编辑解决方案**。用户仅需要写几行代码，即可完成简单的图片编辑操作。详见 [简易图片编辑](/solution/image-editing)🏷️ 。

## 如何开始？

建议先阅读 [快速开始](/quick-tour/quickstart)🏷️ 与 [设计理念](/quick-tour/philosophy)🏷️ ，然后按需阅读 [解决方案](/solution)🏷️ 与 [教程](/tutorial)🏷️ 中的相关章节。如果在过程中遇到问题，可以按照 [参与指引](/quick-tour/participation)🏷️ 联系我们。

## 来点眼前一亮的东西？

### 解决方案展示：通用图片数据增强

作为深度学习的最佳实践之一，[数据增强](https://en.wikipedia.org/wiki/Data_augmentation)方法被广泛应用在计算机视觉领域学术研究、工业落地的模型训练过程。vkit 内置了丰富的 [通用图片数据增强](/solution/data-augmentation)🏷️ 策略，包括**仿射变换、MLS、相机模型成像、色彩、模糊度、噪点、环境效果、条纹**等不同维度的多种策略实现，帮助用户**高效、高质量**地扩充训练数据集，从而增强模型的泛化性与最终效果。

以下是 vkit 数据增强解决方案的可视化效果展示。

:::tip

某些移动端浏览器可能无法自动播放下面的视频，需要您手动点击播放按钮。

:::

原始图片：

<div align="center">

<img alt="original-combined.jpg" src="docs-resource/quick-tour/introduction/original-combined.jpg" />

<p>注：左边是是原始图片，右边是人像区域的多边形标注的可视化效果。</p>

</div>

应用数据增强策略后的可视化效果:

<div align="center">

<video autoplay="true" muted="true" playsinline="true" loop="true" controls="true">
<source src="docs-resource/quick-tour/introduction/geometric.mp4" type="video/mp4" />
</video>

<p>注：以上展示的是几何畸变增强策略。<code>-polygon</code> 后缀，展示多边形同态变换的结果。</p>

</div>

<div align="center">

<video autoplay="true" muted="true" playsinline="true" loop="true" controls="true">
<source src="docs-resource/quick-tour/introduction/photometric.mp4" type="video/mp4" />
</video>

<p>注：以上展示的是光度畸变增强策略。光度畸变不涉及几何变化，故不展示多边形效果。</p>

</div>

### 解决方案展示：文字检测合成数据

在 [vkit-x](https://github.com/vkit-x/) 创立之初我们就坚定了一个信念：**要向全世界提供最好的 OCR 与文档智能应用**。而要达成这个目标，就需要配合算法模型的设计获得特定的高质量训练数据：这正是 vkit 项目的目标定位。

通俗来讲，OCR（[Optical Character Recognition](https://en.wikipedia.org/wiki/Optical_character_recognition)，光学字符识别）是一个从**图片**中提取**文字信息**的自动化过程。计算机在处理完一张图片之后，会告诉你图片中**所有文字的位置**，以及每个位置对应的**字符内容**。常见的 OCR 系统包含两个部分，**文字检测**与**文字识别**，通常是先做文字检测，再做文字识别：文字检测负责把图片里所有的文字位置找出来，然后文字识别负责把每个位置的文字认出来。

为了训练**高精度的文字检测模型**，我们需要准备对应的**高质量的文字检测训练数据**。在此，我们非常荣幸地向您展示，本项目中**与众不同、高质量的** [文字检测合成数据](/solution/text-detection)🏷️ 解决方案，其具备以下独特优势：

- **字符级精度标注**。区别于常见的文本行级精度标注的数据合成开源项目，vkit 是**首个**能做到字符级精度标注数据合成的开源项目。
- **合成效果丰富多样**。依托于 通用图片数据增强 ，整合了**图章、条形码、Emoji、图标、图片等**丰富的页面元素，同时**覆盖近乎所有常用字体**。
- **专为文档分析场景打造**。贴合实际落地场景。

以下是文字检测合成数据的示例：

<div align="center">

<img alt="text-detection-1-resized.jpg" src="docs-resource/quick-tour/introduction/text-detection-1-resized.jpg" />

<p>注：上面是两页生成的文档图片。</p>

<img alt="text-detection-2-resized.jpg" src="docs-resource/quick-tour/introduction/text-detection-2-resized.jpg" />

<p>注：左边的是生成的文档页面图片，中间的是文本行级别精度的掩码标注，右边的是文本行级别精度的字体大小标注。</p>

<img alt="text-detection-3-resized.jpg" src="docs-resource/quick-tour/introduction/text-detection-3-resized.jpg" />

<p>注：左上方的是文本区域堆叠的页面图片，右上方的是字符级别精度的掩码标注，左下方的是字符级别精度的高斯分布标注，右下方的是字符级别精度的四边形标注。</p>

</div>

## 如何支持我们？

使用本项目、提交使用反馈，就是对我们最大的支持！

如果您感觉这个项目做得还可以，可以来 [GitHub 仓库](https://github.com/vkit-x/vkit)点个 Star ⭐ 支持一下我们。

如果您想要更进一步支持我们，我们也开通了 [赞助渠道](/quick-tour/sponsorship)🏷️ 。

## 与同组织的其他项目是什么关系？

vkit 是 [vkit-x](https://github.com/vkit-x/)  组织的核心基础开源项目。如果感兴趣，可以看看我们其他的开源项目：

- [vkit-x/vkit-open-model](https://github.com/vkit-x/vkit-open-model)：由 vkit 驱动的、文档智能领域的深度学习模型。
- [vkit-x/wden](https://github.com/vkit-x/wden)：帮助我们训练模型的 Docker 开发环境解决方案。
- [vkit-x/iolite](https://github.com/vkit-x/iolite)：简化常见数据格式文件的读写操作。

## 项目许可证书是？

本项目采用商业许可与 [SSPL 许可](https://www.mongodb.com/licensing/server-side-public-license)共存的双许可模式。

详见 [LICENSE.txt](https://github.com/vkit-x/vkit/blob/master/LICENSE.txt)、[LICENSE_COMMERCIAL.txt](https://github.com/vkit-x/vkit/blob/master/LICENSE_COMMERCIAL.txt)、[LICENSE_SSPL.txt](https://github.com/vkit-x/vkit/blob/master/LICENSE_SSPL.txt)。