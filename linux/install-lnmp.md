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

## 配置 Nginx

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
