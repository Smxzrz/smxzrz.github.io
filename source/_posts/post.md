---
layout: my
title: post
date: 2022-07-11 22:08:34
tags: 问题
---

## 关闭电脑占用的端口

### 这是部署hexo遇到的问题

在部署hexo时，在自己电脑上hexo s时无法停止，这样就导致4000端口一直被占用，下次无法启动，所以需要强行关闭

### 查看端口使用情况

命令如下，端口看自己情况，这里是4000端口

```shell
netstat -ano | findstr 4000
```

![查看端口使用情况](https://cdn.jsdelivr.net/gh/Smxzrz/blog-imgbed/blog-img/202207112216784.png)

### 关闭进程

可以看出进程号为44996，到时候关闭自己的要根据自己查出来的进行替换

```
taskkill -PID 44996 -F
```

![关闭进程](https://cdn.jsdelivr.net/gh/Smxzrz/blog-imgbed/blog-img/202207112218818.png)

可以看出成功关闭了