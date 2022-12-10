---
title: crontab 定时任务调度
categories: 系统
tags: Linux
---
### crontab 定时任务调度

`crontab [选项]`

- -e ：编辑crontab定时任务
- -i ：查询crontab 任务
- -r ：删除当前用户所有crontab任务

```shell
# 每分钟在etc执行ls -l命令，并追加到tmp目录下to.txt文件
crontab -e
*/1 **** ls -l /etc/ >/tmp/to.txt
```

```shell
# 备份mysql数据库,每天凌晨02：00备份mysql数据库
crontab -e 
0 2 * * * mysqldump -u root -proot testdb > /home/db.bak
```
