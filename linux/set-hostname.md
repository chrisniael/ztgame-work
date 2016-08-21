# 修改 hostname

## CentOS/RHEL 7

通过 `hostnamectl` 来设置 hostname

```
hostnamectl set-hostname dog.shenyu.me
```

查看设置结果

```
hostnamectl status
```

不需要重启系统，只需要重新 SSH 登陆就能查看到修改后的结果


## CentOS/RHEL 6

### 临时修改 hostname

```
hostname dog.shenyu.me
```

查看修改后的结果

```
hostname
```

这种修改方式只能临时修改 hostname，系统重启后就会恢复之前的 hostname。

### 永久性修改 hostname

```
vim /etc/sysconfig/network
```

编辑 `/etc/sysconfig/network`， 将 `HOSTNAME` 字段为想设置的 hostname

```
HOSTNAME=dog.shenyu.me
```

这种方式需要重启，才能使设置 hostname 生效。
