# 🏳 简易修改变形器，平面在弯曲模式下不发生形变？

## 现象

<figure><img src="../.gitbook/assets/弯曲模式不形变.gif" alt=""><figcaption></figcaption></figure>

## 原因

{% hint style="info" %}
[https://www.bilibili.com/video/BV12J411m7Sh/?vd\_source=15155de7c71a11fde776b09c8204609a](https://www.bilibili.com/video/BV12J411m7Sh/?vd\_source=15155de7c71a11fde776b09c8204609a)
{% endhint %}

首先需要理解弯曲的工作原理，这里有两个定义<mark style="color:red;">**工作轴(**</mark><mark style="color:purple;">**形变轴**</mark><mark style="color:red;">**)**</mark>和<mark style="color:red;">**旋转轴(**</mark><mark style="color:purple;">**弯曲轴**</mark><mark style="color:red;">**)**</mark>

假设我们知道了工作轴X和弯曲轴Y如下

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

首先 blender会按照工作轴找到起点和终点， 然后按照输入的角度，尝试将起点和终点弯曲相遇。

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

因此我们需要确定当前的工作轴和弯曲轴，以及其中的对照关系 ，对照表如下

| 旋转轴 | 工作轴 |
| --- | --- |
| Z   | X   |
| X   | Z   |
| Y   | Z   |

以第一组为例，假设我们将旋转轴定义为Z，那么工作轴就是X , 回到最初的问题，为什么平面没有产生形变？

我们把旋转轴设置为了X，那么对照表 ，工作轴就是Z。  blender 从Z轴找起点和终点，但是<mark style="color:red;">**Z轴上是一个面，厚度为0**</mark>，起点和终点重合，因此就无法发生形变。将旋转轴设置为Y同理。

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

那么如何处理才能弯曲？ 如果设置为X轴为旋转轴，那么需要将Z轴上有厚度才行， 此时在编辑模式将面添加细分，并且将平面按照X轴旋转即可



