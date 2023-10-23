---
description: >-
  官方文档:
  https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/array.html
---

# 🖍 阵列修改器

## 使用场景

有些时候，需要复制出很多相同的对象，就可以使用阵列修改器

## 适配类型

### 固定数量

按照指定数量的副本复制对象

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt=""><figcaption><p>固定数量</p></figcaption></figure>

### 适配长度

给定一个固定的长度，然后blender会生成足够的副本，以符合 _长度_ 给定的固定长度

{% hint style="info" %}
此处需要给出物体长度的整数倍, 如果不给整数倍, 会向上取整

![](<../.gitbook/assets/image (3) (1) (1) (1).png>)
{% endhint %}

### 适配曲线

给定一个曲线，在适配的曲线路径指定的长度范围内生成指定数量的副本。

<figure><img src="../.gitbook/assets/Kapture 2023-10-09 at 20.25.18.gif" alt=""><figcaption><p>适配曲线</p></figcaption></figure>

### 偏移属性

#### 相对偏移

模型的边界框长度乘以一个指定的系数，当做偏移量

#### 恒定偏移

以常量为单位进行偏移，偏移的距离跟物体本身没关系

#### 物体偏移

将从对象（相对于当前对象）进行的变换添加到偏移中。 需要借助额外的参考物体实现。

假如建立一个空的物体，对空的物体的修改会影响到复制 出来的模型。

<figure><img src="../.gitbook/assets/Kapture 2023-10-11 at 07.51.02.gif" alt=""><figcaption><p>物体偏移</p></figcaption></figure>

比如修改了缩放属性，复制出来的模型会跟着改变

<figure><img src="../.gitbook/assets/Kapture 2023-10-11 at 07.59.12.gif" alt=""><figcaption></figcaption></figure>

### 合并

在指定的 _距离_ 内，每个副本中的顶点会和下一个副本中的顶点合并。

合并是为了防止重叠点的问题。

<figure><img src="../.gitbook/assets/Kapture 2023-10-11 at 08.03.43.gif" alt=""><figcaption></figcaption></figure>
