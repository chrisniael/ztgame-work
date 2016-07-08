# 安装 POSIX 手册

当前操作系统

```shell
cat /etc/centos-release
```

> CentOS Linux release 7.2.1511 (Core)

使用 yum 来安装 POSIX 手册，记得先切换成 root 账号

```shell
su - root
yum install man-pages libstdc++-docs
```
