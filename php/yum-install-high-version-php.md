# YUM 安装高版本 PHP

## 添加 Webtatic 源


**CentOS/RHEL 7**

```shell
rpm -Uvh https://mirror.webtatic.com/yum/el7/latest.rpm
```

**CentOS/RHEL 6**

```shell
rpm -Uvh https://mirror.webtatic.com/yum/el6/latest.rpm
```

**CentOS/RHEL 5**

```shell
rpm -Uvh https://mirror.webtatic.com/yum/el5/latest.rpm
```

## 安装 PHP

```shell
yum install php56w php56w-common php56w-fpm php56w-mysql -y
```

这里安装的是 `php 5.6` 版本的，可选 `php 5.4`、`php 5.5` 还有 `php 7.0` 版本。例如，如果要安装 `php 7.0`

```shell
yum install php70w php70w-common php70w-fpm php70w-mysql -y
```
