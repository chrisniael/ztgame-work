# RedHat 替换 yum 源

RedHat 自带的 yum 源是需要注册（收费）才是更新下载软件的，如果你没有注册就使用，则会报下面的错误

```
This system is not registered to Red Hat Subscription Management. You can use subscription-manager to register.
```

可以将自带的 yum 源替换为 CentOS 源即可。


## 删除 RedHat 自带的 yum

```shell
rpm -qa | grep yum | xargs rpm -e --nodeps
```

## 下载并安装新的 yum 和 yum 源

查看系统版本

```shell
cat /etc/redhat-release
```

```
Red Hat Enterprise Linux Server release 6.4 (Santiage)
```

根据上面的系统版本（RedHat 6.4），进入系统对应目录 

* [CentOS 7](http://mirrors.163.com/centos/7/os/x86_64/Packages/)
* [CentOS 6](http://mirrors.163.com/centos/6/os/x86_64/Packages/)
* [CentOS 5](http://mirrors.163.com/centos/5/os/x86_64/Packages/)

下载下面这三个 rpm 包，有新版本的话，推荐安装新版本

* [yum-metadata-parser-1.1.2-16.el6.x86_64.rpm](http://mirrors.163.com/centos/6/os/x86_64/Packages/yum-metadata-parser-1.1.2-16.el6.x86_64.rpm)
* [yum-3.2.29-73.el6.centos.noarch.rpm](http://mirrors.163.com/centos/6/os/x86_64/Packages/yum-3.2.29-73.el6.centos.noarch.rpm)
* [yum-plugin-fastestmirror-1.1.30-37.el6.noarch.rpm](http://mirrors.163.com/centos/6/os/x86_64/Packages/yum-plugin-fastestmirror-1.1.30-37.el6.noarch.rpm)

安装下载下来的 rmp 包

```shell
rpm -ivh yum-metadata-parser-1.1.2-16.el6.x86_64.rpm
rpm -ivh yum-3.2.29-73.el6.centos.noarch.rpm
rpm -ivh yum-plugin-fastestmirror-1.1.30-37.el6.noarch.rpm
```

下载系统对应的 repo 文件，放入 `/etc/yum.repos.d/`（最好先备份旧文件，如果文件名一样的话）

* [CentOS 7](http://mirrors.163.com/.help/CentOS7-Base-163.repo)
* [CentOS 6](http://mirrors.163.com/.help/CentOS6-Base-163.repo)
* [CentOS 5](http://mirrors.163.com/.help/CentOS5-Base-163.repo)

```shell
cd /etc/yum.repos.d/
wget http://mirrors.163.com/.help/CentOS6-Base-163.repo
```

## 清除原有的缓存，重建缓存

```shell
yum clean all
yum makecache
```

## 更新系统

```shell
yum update
```
