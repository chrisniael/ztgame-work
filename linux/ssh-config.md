# 解决 SSH 自动断开

## 客户端设置

```sh
sudo su -
vim /etc/ssh/ssh_config
```

添加下面内容

```
ServerAliveInterval 60
```

这样，连接 SSH 时，每60秒就会发一个 KeepAlive 请求，避免断开连接


## 服务器设置
