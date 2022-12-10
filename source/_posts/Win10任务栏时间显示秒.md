---
title: Win10任务栏时间显示秒
categories: 系统
tags: windows
---


1. 打开注册表：win+R 输入regedit
2. 找到`HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced`
3. 在Advanced上新建 DWORD(32位)值，命名为：`ShowSecondsInSystemClock`，双击打开将数值数据改为1，并点击确定，关闭注册表。
4. 重启电脑，就可以实现秒的显示。如果不重启电脑，则在任务管理中找到“Windows资源管理器”，鼠标右键选择“重新启动”。

```bat
reg add "HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v ShowSecondsInSystemClock /t REG_DWORD /d 1 /f
```
