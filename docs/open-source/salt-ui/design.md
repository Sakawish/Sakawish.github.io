# 设计

SaltUI 以清新的设计，给人稳定成熟的感觉。

## 边距

SaltUI 将列表设计分为内外两层： 外层（必须）：背景，可以填充默认色 background 或者自定义背景图片，background 不允许透明度 内层（可选）：用以显示内容，填充默认色 subBackground ，subBackground 可根据需要设置透明程度。

当使用内层的时候，内层应该被 RoundedColumn 包裹，或自定义包裹器。

包裹器竖向外边距为 8 dp ，横向外边距为 16 dp ，包裹器不应设置内边距。

列表项目的最小高度应该设置为 56 dp ，竖向内边距为 12 dp ，横向外边距为 16 dp。

列表中元素与元素的边距应该设置为 12 dp ，若为竖向文本间应该设置为 2 dp。

## 高度

项、按钮、边框应以 56 dp 做为高度。

## 阴影

如非特殊需要，则在 SaltUI 中**不**应该使用阴影。

## 文本

主要文本 16 sp ，次要文本 13 sp （或 12 sp）。

### 文本编排建议

段落或者句子结尾不写句号。