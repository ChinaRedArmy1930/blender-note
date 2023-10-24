# ❓ 使用阵列修改器中物体偏移复制的时候物体大小发生变化？

## 模型现象

使用阵列修改器，物体偏移，锚定了一个空对象，复制后物体变大或者变小

<figure><img src="../.gitbook/assets/阵列修改器-物体大小变化.gif" alt=""><figcaption></figcaption></figure>

## 处理方法

将模型的缩放比例和空对象缩放比例设置为1.0, 物体大小就会一致

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption><p>空对象缩放比例</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption><p>模型比例缩放</p></figcaption></figure>

## 问题分析

此处的计算方法为, 第二个及后面的复制对象，都是按照第一个的原始尺寸计算 ✖️ 空对象的缩放比例

因此, 如果想要复制的模型保持不变，就需要保证 原始尺寸计算 ✖️ 空对象的缩放比例  不变&#x20;

例如， 设置第一个缩放比例为2 , 此时就需要设置空对象的缩放比例也是2， 也就是&#x20;

<mark style="color:red;">**物体模型的缩放比例 = 空对象的缩放比例**</mark>



