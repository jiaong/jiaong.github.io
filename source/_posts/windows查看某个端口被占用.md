---
title: windows如何查看某个端口被谁占用
categories: 系统
tags: windows
---


- 开始---->运行---->cmd，或者是`Window+R`组合键，调出命令窗口

- 输入命令：`netstat -ano`，列出所有端口的情况。
- 查看被占用端口对应的PID，输入命令：`netstat  -aon|findstr "50000"`
- 继续输入`tasklist|findstr "PID"`，回车，查看是哪个进程或者程序占用了PID端口。
- 在任务管理器的进程里找到PID，手动结束对应的进程。
- 或者cmd的命令窗口中输入：`taskkill /f /t /im  ****.exe`。
