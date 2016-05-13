# SELinux


## 临时设置 SELinux 模式

```shell
setenforce 0
```

* 0 表示 enforcing 模式
* 1 表示 permissive 模式
* 重启后会失效, 修改 `/etc/selinux/config` 永久生效

## /etc/selinux/config

```shell
SELINUX=disabled
```

可配置的值
  
* enforcing - 开启 SELinux 安全策略
* permissive - 不开启 SELinux，而是发出警告
* disabled - 完全关闭 SELinux

## 注意

当 SELinux 配置为 enforcing 模式时，会导致 ssh authorized_keys 配置失效。
