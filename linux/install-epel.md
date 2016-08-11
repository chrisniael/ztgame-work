# 安装 EPEL 源

EPEL 是 Extra Packages for Enterprise Linux 的缩写，它是 Fedora Special Interest Group 为 企业 Linux 创建、维护并管理的额外的高质量包集。支持包括 Red Hat Enterprise Linux (RHEL)，CentOS，Scientific Linux (SL)，Oracle Linux (OL) 等。

## 查看系统版本

```shell
cat /etc/centos-release
```

```
CentOS Linux release 7.2.1511 (Core)
```

## 安装 EPEL

根据系统版本来安装对应的 EPEL，这里是 CentOS 7

```shell
yum install http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-5.noarch.rpm
```

或者

```shell
yum install epel-release
```

## 检查已经安装的源

```shell
yum repolist
```

## 参考

[EPEL Wiki (fedoraproject.org)](https://fedoraproject.org/wiki/EPEL)
