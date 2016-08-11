# PHP-FPM 监听 Unix Socket

PHP-FPM 默认监听 localhost (127.0.0.1)  9000 端口，通过下面的配置，可以更改 PHP-FPM 监听 Unix Socket。

## 修改 PHP-FPM 配置

编辑 `/etc/php-fpm.d/www.conf`

```shell
vi /etc/php-fpm.d/www.conf
```

找到下面这行内容

```
listen = 127.0.0.1:9000
```

将其更改为

```
listen = /var/run/php-fpm/php5-fpm.sock
```

重启 PHP-FPM

```shell
systemctl restart php-fpm
```

## 修改 Nginx 配置

编辑 `/etc/nginx/nginx.conf`

```shell
vi /etc/nginx/nginx.conf
```

找到下面这行内容

```
fastcgi_pass    127.0.0.1:9000;
```

将其修改为

```
fastcgi_pass    unix:/var/run/php-fpm/php5-fpm.sock;
```

重启 Nginx

```shell
systemctl restart nginx
```
