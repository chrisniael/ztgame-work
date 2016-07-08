# 安装 POSIX 手册

最小安装的 Linux 没有包含 POSIX 手册，需要手动安装。

使用 yum 来安装 POSIX 手册，记得先切换成 root 账号

```shell
su - root
yum install man-pages libstdc++-docs
```
