# 安装 LEMP

下面安装步骤是基于 `CentOS 7` 的。

官方 CentOS yum 源里是不存在 `Nginx` 的，所以首先需要安装 `EPEL`。请参考 [CentOS 安装 EPEL]()。
 
## 安装 Nginx

* 使用 `yum` 安装 `Nginx`

    ```
    yum install nginx -y
    ```

* 启动并设置 `Nginx` 开机自动启动

    ```shell
    systemctl start nginx
    systemctl enable nginx
    ```

* 如果你开启了防火墙，则需要设置允许 `Nginx` 通过

    ```shell
    firewall-cmd --permanent --add-service=http
    systemctl restart firewalld
    ```

现在你可以打开 `http//ip-address` 来查看 `Nginx` 是否正常工作。

### 配置 Nginx

* 打开 `Nginx` 配置文件 `/etc/nginx/nginx.conf`

    ```shell
    vi /etc/nginx/nginx.conf
    ```

* 设置 `worker_processes` 为适当的值（一般设置为 CPU 的核数，我的电脑是单核的，所以就设置为 `1`）

    ```shell
    worker_processes 1;
    ```

* 修改 `server_name`，并添加下面的配置

    ```shell
    [...]
    server {
        listen       80;
        server_name  server.unixmen.local;
        root         /usr/share/nginx/html;
    [...]

        location ~ \.php$ {
            root           /usr/share/nginx/html;
            fastcgi_pass   127.0.0.1:9000;
            fastcgi_index  index.php;
            fastcgi_param  SCRIPT_FILENAME  $document_root$fastcgi_script_name;
            include        fastcgi_params;
            }

    [...]
    ```

* 重启 `nginx` 使配置生效（请确保 `php-fpm` 已安装，否则会出错）

    ```shell
    systemctl restart nginx
    ```


## 安装 MariaDB

MariaDB数据库管理系统是MySQL的一个分支，主要由开源社区在维护，采用GPL授权许可。MariaDB的目的是完全兼容MySQL，包括API和命令行，使之能轻松成为MySQL的代替品。

使用 yum 安装 MariaDB

```shell
yum install mariadb-server mariadb -y
```

启动 MariaDB，并设置为开机自动启动
```shell
systemctl start mariadb
systemctl enable mariadb
```

### 设置 MySQL root 用户密码

MySQL 默认没有设置 root 的密码，执行下面指令来设置 root 密码

```shell
mysql_secure_installation
```

## 安装 PHP

通过 yum 来安装 php

```shell
yum install php php-common php-fpm php-mysql -y
```

启动 php-fpm，并设置 php-fpm 开机自动启动

```shell
systemctl start php-fpm
systemctl enable php-fpm
```

### 配置 PHP

打开 `/etc/php.ini`，修改 `cgi.fix_pathinfo` 的值为 `0`

```shell
vi /etc/php.ini
```

```
[...]
cgi.fix_pathinfo=0
[...]
```

打开 `/etc/php-fpm.d/www.conf`，修改用户和组为 `nginx`

```
vi /etc/php-fpm.d/www.conf
```

```
[...]
; Unix user/group of processes
; Note: The user is mandatory. If the group is not set, the default user's group
;       will be used.
; RPM: apache Choosed to be able to access some dir as httpd
user = nginx
; RPM: Keep a group allowed to write in log dir.
group = nginx
[...]
```

重启 php-fpm

```shell
systemctl restart php-fpm
```

## 参考资料

* [Install LEMP Server On CentOS 7](http://www.unixmen.com/install-lemp-server-nginx-mariadb-php-centos-7/)
