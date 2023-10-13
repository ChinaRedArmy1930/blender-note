---
description: >-
  官方文档：https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/bevel.html
---

# 📀 倒角修改器

## 关键属性

### 宽度类型

#### 偏移量

#### 宽度

#### 深度

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="375"><figcaption></figcaption></figure>

### 限定方式

#### 无

无限制，所有的棱将会倒角。

#### 角度

只对相邻面法线的角度加上定义的 _角度_ 小于180度的边缘进行倒角。

#### 权重

使用每个边的倒角权重来确定倒角的宽度。当倒角权重取 0.0 时，不会应用倒角。

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

#### 顶点组

用一个顶点组的权重，来确定该倒角面的宽度。当倒角权重取0.0时，不会应用倒角。

使用如下方法设置顶点组

<figure><img src="../.gitbook/assets/Kapture 2023-10-12 at 08.01.33.gif" alt=""><figcaption><p>顶点组</p></figcaption></figure>

如果使用反转的话，就会对其他点进行倒角

<figure><img src="../.gitbook/assets/Kapture 2023-10-12 at 07.50.35.gif" alt=""><figcaption><p>反转顶点组</p></figcaption></figure>



