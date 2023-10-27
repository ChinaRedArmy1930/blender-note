---
description: >-
  官方文档:https://docs.blender.org/manual/zh-hans/4.1/render/shader_nodes/input/fresnel.html
---

# ⌨ 菲涅耳节点

## 菲涅耳概念

[UNITY DOC ](https://docs.unity3d.com/cn/2021.1/Manual/StandardShaderFresnel.html)

[介绍](https://www.voidsky.cn/2020/02/20/%E8%AE%A1%E7%AE%97%E6%9C%BA%E5%9B%BE%E5%BD%A2%E5%AD%A6%EF%BC%9A%E8%8F%B2%E6%B6%85%E5%B0%94%E6%95%88%E5%BA%94-Fresnel-Effect/)

[B站的一个介绍](https://www.bilibili.com/video/BV1i14y1M7Bz/?spm\_id\_from=333.788\&vd\_source=15155de7c71a11fde776b09c8204609a)

对非金属(比如水)来说， 平行于是水面的光线反射强烈，垂直于水面的光线反射效果差

举个例子，下面这个没有菲涅尔效果，注意猴子的眼睛，可以看到反射的光线&#x20;

{% hint style="danger" %}
注意漫射和光泽的节点输入位置， 光泽必须要在上面
{% endhint %}

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

这是添加了菲涅尔的效果 ，注意眼睛中间，已经不反射光线了

<figure><img src="../../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

原理化BSDF内置了这种菲涅尔的效果， 可以看到，当系数差不多时，效果也是差不多的

<figure><img src="../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>
