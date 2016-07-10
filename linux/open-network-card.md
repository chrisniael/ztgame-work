# 打开网卡

Minimal 安装的 CentOS 默认启动时不开启网卡，所以需要手动将其设置为启动时打开。

* `cd /etc/sysconfig/network-scripts/`
* 编辑文件 `ifcfg-eth0`（文件名可能不一致，但命名规则一定是以 `ifcfg` 为前缀，再加上网卡的名字），`vim ifcfg-eth0`
* 将其中的 `ONBOOT=no` 改为 `ONBOOT=yes`
* 然后再重启网络服务，`service network restart`
