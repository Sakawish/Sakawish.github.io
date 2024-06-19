# 文档

主要源码位于文件夹 ui/src/main/java/com/moriafly/salt/ui/ 下。

## SaltTheme 主题

- configs 一些配置，如深色模式；
- colors 颜色；
- textStyles 文本样式；
- dimens 边距等。

如在 Activity 等使用 Compose ，应当使用 SaltTheme 包裹，函数：

```kotlin
@Composable
fun SaltTheme(
    configs: SaltConfigs,
    colors: SaltColors = SaltTheme.colors,
    textStyles: SaltTextStyles = SaltTheme.textStyles,
    dimens: SaltDimens = SaltTheme.dimens,
    content: @Composable () -> Unit
)
```

## SaltConfigs

- isDarkTheme 是否为深色模式，在 Composable 中即可调用 SaltTheme.configs.isDarkTheme 判断当前主题，并根据此调整某些自定义内容。独立于判断系统是否为深色，更适合自定义。

## SaltColors

- highlight 主题色
- text 主文本色
- subText 次文本色
- background 主背景色
- subBackground 次背景色

实现 Android 12 及以上版本的动态颜色主题，需要自行添加 Compose Material3 依赖，并传入 ColorScheme 到函数 saltColorsByColorScheme 或自行完成颜色映射。

```kotlin
fun saltColorsByColorScheme(
    colorScheme: ColorScheme
): SaltColors
```

## SaltTextStyles

- main 主要文本样式
- sub 次要文本样式
- paragraph 大型段落文本样式

## SaltDimens

为 SaltUI 中元素编排边距的设定。

- corner 标准圆角
- dialogCorner 对话框圆角
- outerHorizontalPadding 外部横向边距
- innerHorizontalPadding 内部横向边距
- outerVerticalPadding 外部竖向边距
- innerVerticalPadding 内部竖向边距
- contentPadding 外/部元素边距（不涉及内外层相连）

## Item 组件

Item 组件主要用于构建**内部**竖向页面。

Item 组件应该用于 RoundedColumn 等次背景上，例：

```kotlin
RoundedColumn {
    ItemTitle(text "SaltUI")
    Item(
        onClick = {
            // TODO
        },
        text = "Hello, Sakawish!"
    )
}
```

### ItemTitle
### ItemText
### Item
### ItemSwitcher
### ItemPopup
### ItemCheck
### ItemValue
### ItemEdit
### ItemEditPassword
### ItemSlider
### ItemSpacer
### ItemContainer

## UnstableSaltApi 注解

表示此组件或者方法非稳定。

## .ext 包拓展

### ContextExt

用以在 Composable 中获取 Activity。

```kotlin
Context.findActivity()
```

### WindowInsetsExt

获取 systemBars + displayCutout。

```kotlin
WindowInsets.Companion.safeMain
```

## Animate 动画

### animateInfiniteRotationState