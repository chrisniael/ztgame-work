# svn 命令智能补全

在 bash 中，svn 命令默认是不会想 bash 命令那样自动补全的，使用起来尤其不方便，其实 Linux 有提供了 svn 智能补全的脚本文件 ( `/etc/bash_completion.d/subversion` )，只要配置一下随 bash 启动执行这个脚本就OK了。

## 配置 bash

* 执行 `vim ~/.bash_profile` 编辑 `~/.bash_profile` 文件

* 添加下面这段代码，并保存

    ```shell
    if [ -f /etc/bash_completion.d/subversion ]
    then
        source /etc/bash_completion.d/subversion
    fi
    ```

配置完成之后，重启 bash，或者执行 `source ~/bash_profile` 一下，就能使配置生效，之后执行 svn 命令的时候就能像在 bash 中一样使用 `Tab` 键来补全 svn 命令了。