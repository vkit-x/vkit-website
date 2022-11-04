---
sidebar_position: 2
---

# 快速开始

## 说明

vkit 是一个使用 Python 编程语言编写的项目。对于本章节之后的内容，我们假设读者具备 Python 编程经验。

## 安装

环境要求：
- Python：`3.8` 及以上版本。
  - 基于第三方依赖的稳定性、发布周期、软件质量等方面的考虑，最新发布的 Python 版本可能不会得到 vkit 的立即支持。一般可以承诺的是，如果最新发布的 Python 版本是 `3.X.0`，那么会在 Python `3.X.1` 版本发布后得到 vkit 的支持。
- 主流的操作系统。
  - Linux 与 macOS 会得到充分的测试。
  - Windows 会得到尽力支持。目前我们没有 Windows 开发环境以及对应的 CI，未来会根据用户反馈按需修正补齐。

使用以下命令，安装最新的稳定版本：

```bash
pip install vkit
```

或者，使用以下命令，安装主分支的最新版本：

```bash
pip install vkit-nightly
```

## 验证

可以通过执行下面的代码片段验证 vkit 的功能性。

这段代码从文件系统中加载一张图片，然后将图片顺时针旋转 30 度，最后输出旋转后图片到某个路径。

```python
from vkit.element import Image
from vkit.mechanism.distortion import rotate

# Change to your paths.
image_file = '/path/to/Rooster.jpg'
output_file = '/path/to/Rooster-angle-30.jpg'

# Load image.
image = Image.from_file(image_file).to_rgb_image()
# Rotate image.
rotated_image = rotate.distort_image({'angle': 30}, image=image)
# Save image.
rotated_image.to_file(output_file)
```

执行结果：

<div align="center">

<img alt="1.jpg" src="/docs-resource/quick-tour/quickstart/demo.jpg" />

</div>

左边是原图（可以从[这里](https://github.com/vkit-x/vkit-dataset/raw/master/Rooster.jpg)获得），上方的代码片段成功运行后，会得到右边的图片。

如果已经成功运行，恭喜，您已经成功安装了 vkit 🎉。