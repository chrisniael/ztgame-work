# 域名解析配置


## /etc/hosts

定义了IP对应的主机名


## /etc/host.conf

```shell
order hosts, bind
multi on
nospoof on
```

`order hosts, bind` 指定了主机名的解析顺序先从hosts中查找，然后到dns服务器的记录里查找。

`multi on` 是允许一个主机名对应多个IP地址，拥有多个IP地址的主机一般称为多穴主机。

`nospoof on` 指不允许对服务器尽心IP地址欺骗。IP欺骗是一种攻击系统安全的手段，通过把IP地址伪装成别的计算机，来取得其它计算机的信任。


## /etc/resolv.conf

```shell
options attempts:1 timeout:1 rotate
nameserver 8.8.8.8
nameserver 114.114.114.114
```

配置完成后，可以执行 `service network restart` 来生效。
