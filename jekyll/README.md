# Jekyll

## 修改 RubyGems 镜像源

    ```shell
    gem sources -a https://ruby.taobao.org/
    gem sources --remove https://rubygems.org/
    ```

    查看当前镜像源，确保输出的只有 `https://ruby.taobao.org/`

    ```shell
    gem sources -l
    ```

## 安装 jekyll

    * Mac OS X 10.11.4

    ```shell
    su -
    gem install jekyll rouge -V
    ```

    * CentOS 7.0

    ```shell
    su -
    yum install -y ruby ruby-devel rubygems
    gem install jekyll jekyll-paginate -V
    ```

# 更新 Ruby 库

推荐升级一下 Ruby 的库，否则可能会出现使用上的问题。

```shell
gem update --system
```

先更新一下 Gem 自身，然后再使用 Gem 更新 Ruby 的各种库

```shell
gem update
```

Mac 可能会应为 SIP 出现文件读写权限问题，请参考 [SIP](../mac/sip.md) 这篇文章来暂时先关闭 SIP，升级完 Ruby 库后，再开启 SIP。

# 安装 Jekyll-Assets

```
gem install jekyll-assets -V
```
