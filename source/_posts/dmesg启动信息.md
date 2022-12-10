---
title: dmesg启动信息
categories: 系统
tags: Linux
---

### 1. 搜索包含特定字符串的被检测到的硬件

由于‘dmesg’命令的输出实在太长了，在其中搜索某个特定的字符串是非常困难的。因此，有必要过滤出一些包含‘usb’ ‘dma’ ‘tty’ ‘memory’等字符串的日志行。grep 命令 的‘-i’选项表示忽略大小写。

```bash
dmesg | grep -i usb
dmesg | grep -i dma
dmesg | grep -i tty
dmesg | grep -i memory
```

### 2. 清空dmesg缓冲区日志

我们可以使用如下命令来清空dmesg的日志。该命令会清空dmesg环形缓冲区中的日志。但是你依然可以查看存储在`/var/log/dmesg`文件中的日志。你连接任何的设备都会产生dmesg日志输出。
`dmesg -c`

### 3. 实时监控dmesg日志输出

在某些发行版中可以使用命令`tail -f /var/log/dmesg`来实时监控dmesg的日志输出。
**查看：**
`watch "dmesg | tail -20"`

**结论:**

dmesg命令在系统dmesg记录实时更改或产生的情况下是非常有用的。你可以使用man dmesg来获取更多关于dmesg的信息。
