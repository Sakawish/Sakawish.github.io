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