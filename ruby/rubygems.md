#RubyGems

* 更新 Gem 自身（在某些 Linux 发行版中为了系统的稳定性此命令禁止执行）

    ```shell
    gem update --system
    ```

* 从 Gem 源安装 Gem 包

    ```shell
    gem install [gemname]
    ```

* 从本地安装 Gem 包

    ```shell
    gem install -l [gemname].gem
    ```

* 安装指定版本的 Gem 包

    ```shell
    $ gem install [gemname] --version=[ver]
    ```

* 更新所有安装了的 Gem 包

    ```shell
    $ gem update
    ```

* 更新指定的 Gem 包

    ```shell
    $ gem update [gemname]
    ```

* 删除 Gem 包（注意此命令将删除这个 Gem 包的所有版本）

    ```shell
    $ gem uninstall [gemname]
    ```

* 删除指定版本的 Gem 包

    ```shell
    $ gem uninstall [gemname] --version=[version]
    ```

* 查看本地已安装的所有 Gem 包

    ```shell
    $ gem list [--local]
    ```
