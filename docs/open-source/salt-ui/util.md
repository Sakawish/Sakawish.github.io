# Util 包

位于 com.moriafly.salt.ui 下的 util 包。

## Screen

### 获取屏幕圆角像素半径

通过读取 android.dimen.rounded_corner_radius_top 读取设备屏幕圆角，这个属性需要厂商定义。

各种设备的圆角曲率不同，所有此半径属性也是个大概值，具体实际实现应该考虑在获取到此属性后进行进一步处理，如默认小一些以覆盖不同曲率。

```kotlin
fun getRoundedCornerRadiusTop(context: Context): Int
```