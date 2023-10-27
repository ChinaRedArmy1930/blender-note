---
description: >-
  https://docs.blender.org/manual/zh-hans/4.1/render/shader_nodes/shader/principled.html
---

# 💚 原理化BSDF

## 从输入

### 基础色

用于漫反射、次表面、金属和透射的材质的整体颜色。

### 金属度

电介质和金属材料模型之间的混合。当值为 0.0 时，材质由漫反射或透射基层组成，顶部有镜面反射层。值为 1.0 时会产生用基色着色的完全镜面反射，而没有漫反射或透射。

### 糙度

指定镜面反射和透射表面的微面粗糙度。 值为1时，完全漫反射，设置为0时，完全镜面反射

## 次表面

[次表面散射WIKI](https://zh.wikipedia.org/wiki/%E6%AC%A1%E8%A1%A8%E9%9D%A2%E6%95%A3%E5%B0%84)

### 权重

漫反射表面和次表面散射之间的混合。<mark style="color:red;">**通常应为0或1**</mark>（完全漫反射或次表面）

### 半径

光散射到表面下方的平均距离。<mark style="color:red;">**较高的半径可以使外观更柔和**</mark>，因为光线会流入阴影区域并穿过物体。散射距离是针对RGB通道单独指定的，对于具有较强红光散射的面板材质，渲染效果较佳。X，Y和Z的数值会分别映射到R，G和B的值。

## 镜面反射

### 各向异性过滤/旋转

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption><p>过滤</p></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption><p>旋转 </p></figcaption></figure>

各向异性参数用于添加光泽反射，可以单独控制U和V方向的粗糙度，用户活动的切线是从活动的UV图中得到的，如果没有UV贴图，他们将基于网格边界盒的球体自动生成。

模型表面的反射光线沿着不同角度进行反射。

各向异性参数可以帮我们制作金属拉丝的效果。

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## 光泽

光泽模拟表面上非常小的纤维。对于布料，这会在边缘附近添加柔软的天鹅绒般的反射。它还可用于模拟任意材料上的灰尘。

### 权重

从0 到 1 如下图

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## 清漆(图层)

涂在材料的顶部，以<mark style="color:red;">**模拟清漆、清漆或汽车油漆**</mark>等。

### 权重

控制涂层的强度，包括反射和着色。对于基于物理的材料，通常应为零或一，但可以进行纹理化以改变表面上的涂层量。

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption><p>从0 - 1</p></figcaption></figure>

### 粗糙度

<figure><img src="../../../.gitbook/assets/image (5).png" alt=""><figcaption><p>从0 - 1</p></figcaption></figure>

### IOR 折射率

{% hint style="info" %}
部分物体的IOR:[https://pixelandpoly.com/ior.html](https://pixelandpoly.com/ior.html)
{% endhint %}

单独使用这个属性无法工作，需要配合透射属性 。比如可以制作出玻璃的质感。

### Alpha

控制表面的透明度，<mark style="color:red;">**数值设定为1.0时，表面完全不透明**</mark>。通常连接到 "图像纹理" 着色器节点的Alpha输出接口。

<figure><img src="../../../.gitbook/assets/image (16).png" alt=""><figcaption><p>Alpha 从 0.0 到 1.0</p></figcaption></figure>



