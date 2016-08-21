# 查看 Linux 虚拟机类型

## CentOS/RHEL 7

```shell
hostnamectl status
```

实例输出

```
   Static hostname: dog.shenyu.me
         Icon name: computer-vm
           Chassis: vm
        Machine ID: 45461f76679f48ee96e95da6cc798cc8
           Boot ID: 2cc49c46dda64a5ebe8f1552015c8746
    Virtualization: kvm
  Operating System: CentOS Linux 7 (Core)
       CPE OS Name: cpe:/o:centos:centos:7
            Kernel: Linux 3.10.0-327.28.2.el7.x86_64
      Architecture: x86-64
```

查看 `Virtualization` 字段就能知道系统的虚拟化类型了。

## CentOS/RHEL 6

CentOS 6 没有 `hostnamectl` 命令，所以只能另寻他路了

```shell
dmesg | grep virtual
```

如果上面命令的输出里有 `kvm` 出现，则使用的是 `kvm` 虚拟化技术。

也可以安装 `virt-what`，来判断虚拟化类型

```shell
yum install virt-what
```

运行 `virt-what` 就会输出当前机器的虚拟化类型。
