# 相关系统适配问题

## 小米 MIUI/Hyper OS

**Q：调用小米妙播无效？**

A：调用小米妙播功能需要 MIUI 12 及以上版本，点击 Salt Player 播放界面右上角按钮自动跳转。此功能基于小米投屏相关系统组件，检测是否禁用了相关组件。

**Q：不支持 MIUI/Hyper OS 小部件？**

A：云端控制，努力过＞︿＜。继续努力。

## 华为鸿蒙

**Q：音乐控制中心不显示？**

A：白名单，努力过＞︿＜。继续努力。

## vivo OriginOS/Funtouch OS

**Q：Hi-Fi 模式里面没有？**

A：由白名单控制。部分 vivo 的设备有 Hi-Fi 模式功能，可以通过 adb 的方式输入 `settings put global game_support_hifi_list com.salt.music` 添加。当然添加其他音乐等软件也可以的，将 `com.salt.music` 改成对应包名。

## OPPO ColorOS

**Q：没有音乐通知？**

A：一般会默认屏蔽 Salt Player 的通知权限，需要手动授予 Salt Player 通知权限。

## 魅族 Flyme

**Q：回到桌面音乐播放会突然暂停？**

A：部分魅族设备（多见于 16 系列）使用 OpenSL ES 输出可能会异常暂停，原因未知，请更换 AudioTrack 等其他输出方式。

**Q：魅族 21 灵动环音乐适配？**

A：暂时不太清楚，估计是白名单或者有特殊适配。