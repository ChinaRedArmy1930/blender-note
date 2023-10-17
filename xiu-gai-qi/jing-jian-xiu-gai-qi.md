---
description: >-
  官方文档:
  https://docs.blender.org/manual/zh-hans/4.1/modeling/modifiers/generate/decimate.html#decimate-modifier
---

# 🦴 精简修改器

## 使用场景

允许你在尽量不改变网格形状的情况下，减少其顶点、面的数量。&#x20;

## 精简模式

### 塌陷

渐进式地合并顶点，有时会按照需要将面变为四边形或者三角形。 可以使用三角化将四边形全部变为三角形。 也可以使用对称，使得精简后保持一个轴上的对称性.

<figure><img src="../.gitbook/assets/精简修改器-塌陷.gif" alt=""><figcaption></figcaption></figure>

### 反细分

可以认为是反向的细分。往往会保证精简后的面为四边形。迭代次数往往是2的整数倍。

> 假如表面细分精度视图层级设置为3， 则反细分设置为6可以还原。

<figure><img src="../.gitbook/assets/反细分.gif" alt=""><figcaption></figcaption></figure>

### 平面

通过限制面之间的角度来精简，精简形成的角度（表面之间）高于设置的角度大小。也就是如果面之间小于设定额角度，就会会被合并。

<figure><img src="../.gitbook/assets/精简-平面.gif" alt=""><figcaption></figcaption></figure>
