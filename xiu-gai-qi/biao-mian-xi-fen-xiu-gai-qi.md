---
description: >-
  官方文档：https://docs.blender.org/manual/zh-hans/latest/modeling/modifiers/generate/subdivision_surface.html
---

# 🎆 表面细分修改器

## 使用场景

用于将网格的面分割成更小的面，使其看起来更平滑。它使您能够通过简单建模和低顶点网格创建复杂的光滑表面。

### Catmull-Clark

默认细分方式&#x20;

#### 通过添加顶点的方式可以保留原来的形状

<figure><img src="../.gitbook/assets/表面细分添加环切.gif" alt=""><figcaption></figcaption></figure>

#### 快捷键

CTRL+1  CTRL+2 CTRL+3  可以创建不同视图层级的表面细分修改器

<figure><img src="../.gitbook/assets/表面细分快捷键.gif" alt=""><figcaption></figcaption></figure>

#### 视图层级

在3D视图或最终渲染里显示的细分级数， 一般给到2或者3就够用了

#### 渲染

渲染代表输出时的视图层级，一般和视图层级保持一致。

### 简单型

只细分曲面，这通常不提供任何平滑
