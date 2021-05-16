---
title: Linux root用户下指定用户执行命令
date: 2021-03-16 17:06:00
tags: 
	- Linux
categories: Linux
---





sudo  -H  -u  用户 命令

```shell
sudo -H -u sonar /home/tools/sonar/sonarqube-7.9.5/bin/linux-x86-64/sonar.sh start
```

