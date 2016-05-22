# 解决 SSH 自动断开

使用 SSH 连接服务器操作时，若干分钟不操作就会被断开连接。

## 客户端设置（推荐）

```sh
sudo su -
vim /etc/ssh/ssh_config
```

添加下面内容

```
ServerAliveInterval 60
```

这样，这台客户端连接 SSH 时，每 60 秒就会向服务器发一个 KeepAlive 请求，避免断开连接。


## 服务器设置

```sh
sudo su -
vim /etc/ssh/sshd_config
```

添加下面内容

```
ClientAliveInterval 60
```

重启 sshd 服务

```sh
service sshd restart
```

这样，任何客户端 SSH 连接这台服务器时，每 60 秒都会向客户端发一个 KeepAlive 请求，避免断开连接。这样会导致安全性降低，所以不推荐这种做法。
