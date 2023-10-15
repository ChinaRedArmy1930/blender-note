---
description: >-
  官方文档：https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/deform/curve.html
---

# 曲线修改器

## 使用场景

_曲线_ 修改器为网格沿着一个曲线物体变形提供了一种简单而高效的方法。

## 简单实用流程

### 首先建立需要形变的物体

{% hint style="info" %}
### 比如一个立方体，在<mark style="color:red;">编辑模式</mark>下修改到合适形状
{% endhint %}

<figure><img src="../.gitbook/assets/添加立方体.gif" alt=""><figcaption></figcaption></figure>

### 然后新建一个曲线，在编辑模式下，将曲线移动到合适的位置

<figure><img src="../.gitbook/assets/曲线移动到合适的位置.gif" alt=""><figcaption></figcaption></figure>

### 新增曲线修改器，将曲线物体选项指向曲线

<figure><img src="../.gitbook/assets/添加曲线修改器.gif" alt=""><figcaption></figcaption></figure>

### 在编辑模式下, 增加立方体环切面，并且将立方体的曲线修改器曲线物体指向这个曲线

<figure><img src="../.gitbook/assets/增加物体环切面.gif" alt=""><figcaption></figcaption></figure>

### 此时我们可以移动物体, 达到我们想要的效果

<figure><img src="../.gitbook/assets/移动物体.gif" alt=""><figcaption></figcaption></figure>

&#x20;







