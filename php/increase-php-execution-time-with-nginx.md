# 增加 PHP 执行时间（With Nginx）

PHP 默认的执行时间为 *30s*。

## php.ini 配置

* 打开 `/etc/php.ini` 配置文件
    
    ```shell
    vim /etc/php.ini
    ```

* 修改 `max_execution_time` 的值为 300（默认是30)，单位：秒

    ```
    max_execution_time=300
    ```

当使用 `PHP-FPM` + `Nginx` 时，`php.ini` 的 `max_execution_time` 字段会失效，要通过配置 `PHP-FPM` 的 `request_terminate_timeout` 字段来设置超时时间。

## PHP-FPM 配置

* 打开 `/etc/php-fpm.d/www.conf` 配置文件

    ```shell
    vim /etc/php-fpm.d/www.conf
    ```

* 取消注释 `request_terminate_timeout` 字段（默认是注释的），并将其值设置为 300

    ```
    request_terminate_timeout=300
    ```

## Nginx 配置

* 打开网站对应的 vhost 配置文件（配置文件的位置可能和我的不太一样）

    ```shell
    vim /etc/nginx/vhost/shenyu.me.conf
    ```

* 在 `location` 域里添加 `fastcgi_read_timeout` 字段

    ```
    location ~ \.php$ {
        #...
        fastcgi_read_timeout 300;
        #...
    }
    ```

如果你想要设置所有站点的超时时间，可以修改 `nginx.conf` 配置

* 打开 `/etc/nginx/nginx.conf` 配置文件

    ```shell
    vim /etc/nginx/nginx.conf
    ```

* 在 `http` 域里添加 `fastcgi_read_timeout` 字段

    ```
    http {
        #...
        fastcgi_read_timeout 300;
        #...
    }
    ```

最后重新加载 PHP-FPM & Nginx，使配置生效

```shell
service php-fpm reload
service nginx reload
```
