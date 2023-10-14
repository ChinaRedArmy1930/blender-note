---
description: >-
  官方文档：  
  https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/mirror.html
---

# 🪞 镜像修改器

## 使用场景

当希望模型沿着某个方向对称, 则可以使用当前修改器

### 传统方法

假设希望物体左右一直保持对称, 可以在编辑模式中点击右上角的镜像, 如下图

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 10.06.19 (1).gif" alt=""><figcaption></figcaption></figure>

这种方法问题在于, 如果在一侧新增一个点, 另一边不会新增，修改也不会跟着修改

### 镜像修改器

首先删除一半的顶点, 然后添加镜像修改。此时镜像的模型会跟着一起修改

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 10.06.19.gif" alt=""><figcaption></figcaption></figure>

#### 切分

当镜像模型的时候，模型跨过了镜像轴， 模型会跨过镜像轴， 此时选择切分，就会将跨过选择轴的模型删除掉

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 22.20.22.gif" alt=""><figcaption></figcaption></figure>

#### 翻转

此时假如希望保留跨过线的部分，剔除掉原来的模型.  就可以使用翻转选项

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 22.28.34.gif" alt=""><figcaption></figcaption></figure>

#### 镜像物体

默认情况下，镜像修改器原点在模型内部，可以通过镜像物体设置镜像的原点，将模型的对称原点设置到想要的地方&#x20;

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 22.33.07.gif" alt=""><figcaption></figcaption></figure>

#### 范围限制

用户在编辑模式下移动顶点时，阻止其穿过镜像平面。

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 22.39.00.gif" alt=""><figcaption></figcaption></figure>

#### 合并

合并掉阈值内的点，防止重叠点

如下图，勾选了合并以后，点的数量变少了，说明确实合并和一些顶点

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 23.05.15.gif" alt=""><figcaption></figcaption></figure>

如果不勾选合并，当应用这个修改器后,  会有如下问题

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 23.07.16.gif" alt=""><figcaption></figcaption></figure>



如果勾选了合并，就会妥善的处理重叠点的问题

<figure><img src="../.gitbook/assets/Kapture 2023-10-14 at 23.08.56.gif" alt=""><figcaption></figcaption></figure>
