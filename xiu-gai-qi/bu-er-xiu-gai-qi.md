---
description: >-
  官方文档：
  https://docs.blender.org/manual/zh-hans/dev/modeling/modifiers/generate/booleans.html
---

# 🥑 布尔修改器

使用场景

利用bool算法，将模型相交的区域计算出来， 然后单独显示

## 交集

目标网格和修改后的网格内部的所有内容都会被保留。如果目标是一个集合，那么只有 _所有_ 的网格内部被保留。

<figure><img src="../.gitbook/assets/Kapture 2023-10-13 at 08.05.40 (1).gif" alt=""><figcaption><p>交集</p></figcaption></figure>

## 并集

目标网格或集合将添加到修改后的网格中，从而删除所有内部面。

<figure><img src="../.gitbook/assets/Kapture 2023-10-13 at 08.06.30 (1).gif" alt=""><figcaption><p>并集</p></figcaption></figure>

## 差集

从修改后的网格中减去目标网格或网格集合（保留目标网格或集合的 _外部_ 的所有内容）。

<figure><img src="../.gitbook/assets/Kapture 2023-10-13 at 08.07.26 (1).gif" alt=""><figcaption><p>差集</p></figcaption></figure>

## 运算物体对象

### 集合

当对多个物体需要进行运算的时候，可以将部分物体指定为集合&#x20;

首先选中需要组成集合的立方体，按快捷键M 新建一个集合&#x20;

