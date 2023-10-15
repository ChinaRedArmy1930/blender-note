---
description: >-
  官方文档:
  https://docs.blender.org/manual/zh-hans/latest/modeling/modifiers/generate/solidify.html#solidify-modifier
---

# 💾 实体化修改器

厚度使用场景

修改器获取任意网格的表面，然后为之添加深度，使之变厚。

### 简单型

#### 关键属性

厚度: 需要实体化的厚度

<figure><img src="../.gitbook/assets/实体化修改器-厚度.gif" alt=""><figcaption><p>厚度</p></figcaption></figure>

偏移量: 介于（-1到1）之间的值，用于定位原始网格内外的实体化输出。内部和外部是由面法向决定的。设置为0.0时，实体化后的输出将以原始网格为中心。

<figure><img src="../.gitbook/assets/实体化修改器-偏移量.gif" alt=""><figcaption></figcaption></figure>

均匀厚度: 通过调整维持尖角的厚度。有时改善质量,但也会增加计算时间。

<figure><img src="../.gitbook/assets/均匀厚度.gif" alt=""><figcaption></figcaption></figure>

边缘

* 填充: 填充内部和外部边之间的间隙

<figure><img src="../.gitbook/assets/边缘-仅填充.gif" alt=""><figcaption></figcaption></figure>

* 仅边沿:是否挤出内侧的偏移面

<figure><img src="../.gitbook/assets/仅边沿.gif" alt=""><figcaption></figcaption></figure>

顶底组: 所选顶点组的权重会乘以\*厚度，所以权重较低的顶点的厚度会比较小。不属于该顶点组的顶点将被当做其权重为零来使用。可以通过反转按钮选择其他的顶点

<figure><img src="../.gitbook/assets/顶点组.gif" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/顶点组反转.gif" alt=""><figcaption></figcaption></figure>

顶点组系数:控制实体化修改器的力度，如果为1则顶点组的影响将会消失

#### 法向

翻转: 翻转所有几何形体的法线（包括内部和外部表面）。

<figure><img src="../.gitbook/assets/法相-翻转.gif" alt=""><figcaption></figcaption></figure>

高质量: 获得更准确的法向的朝向。 通过计算法线来获取更均匀的厚度。这样做有时可以提升质量，但也增加了计算时间。



#### 材质

通过指定不同的值，指定不同的材质。

* 值为 0 则使用相同的材质。
* 值为 1 则使用原始材料正下方的材质。
* 值为 -2 则使用原始材料上方两个单位的材质。

<figure><img src="../.gitbook/assets/材质.gif" alt=""><figcaption></figcaption></figure>

#### 边数据

给内侧，外侧， 边沿设置[折痕](https://docs.blender.org/manual/zh-hans/latest/modeling/meshes/editing/mesh/transform/basic.html#modeling-edges-crease-subdivision) ，会被[表面细分修改器](https://docs.blender.org/manual/zh-hans/latest/modeling/modifiers/generate/subdivision\_surface.html)控制



## 复杂型

可以处理一个面连接三个面的情况

