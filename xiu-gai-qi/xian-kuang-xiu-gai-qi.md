---
description: >-
  官方文档：https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/wireframe.html
---

# 🛫 线框修改器

## 使用场景

_线框_ 修改器通过在其面上迭代，将网格转换为线框，收集所有边并将这些边转换为四边多边形。

## 关键属性

### 厚度

线框的深度或大小。

<figure><img src="../.gitbook/assets/线框-厚度.gif" alt=""><figcaption></figcaption></figure>

### 偏移量

一个在 (-1到1) 之间的值，控制线框是从原网格的内部还是外部生成。设置为零时，_偏移_ 将线框居中于原来的边。  -1 代表全部在内部生成 ，1 代表全部在外部生成。

<figure><img src="../.gitbook/assets/偏移量.gif" alt=""><figcaption></figcaption></figure>

### 边界范围

对于非封闭的模型，优化边界的处理。勾选后，会识别到模型的边界， 协助补全模型。

<figure><img src="../.gitbook/assets/边界范围.gif" alt=""><figcaption></figcaption></figure>

### 替换原物体

如果启用了此选项 ,原始网格将被生成的线框将取代。如果禁用，则在其上生成线框（线框和原物体一起显示出来）。



### 厚(宽)度

#### 均匀

通过调整维持尖角的厚度。有时改善质量,但也会增加计算时间。假设在长立方体中，如果没有勾选该选项，模型较长的变会比较细，较短的变会比较粗。

#### 相对

通过边的长度决定边厚度.更长的边更厚.

<figure><img src="../.gitbook/assets/均匀，相对.gif" alt=""><figcaption></figcaption></figure>

### 折痕边

这个选项适用于与 [表面细分修改器](https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/subdivision\_surface.html) 同时使用时. 启用此选项可在其连接处的边创建折痕,并防止大的弯曲交叉。

<figure><img src="../.gitbook/assets/折痕边.gif" alt=""><figcaption></figcaption></figure>

