# 开发

## Android SDK 28 上 HTTP 请求

AndroidManifest.xml 的 application 标签下添加：

```xml
android:networkSecurityConfig="@xml/network_security_config"
```

新建 network_security_config.xml 文件，内容为：

```xml
<?xml version="1.0" encoding="utf-8"?>
<network-security-config>
    <base-config cleartextTrafficPermitted="true" />
</network-security-config>
```

[网络安全配置](https://developer.android.com/privacy-and-security/security-config?hl=zh-cn)

## Jetpack Compose 性能

Dialog 和 ViewModel 的销毁，在 Dialog 中声明出的 ViewModel 被创建不会因为 Dialog 被关闭而自动销毁的。使用在 Dialog 中应该谨慎使用 ViewModel 或进行手动销毁。