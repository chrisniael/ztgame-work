# 彩色化 svn diff

原生的 `svn diff` 命令是不带颜色区分的，安装 **colordiff**，并配置 svn 默认使用 **colordiff** 作为比较工具。


### 安装 colordiff

* 下载 colordiff 源码包

* 执行 `make` 编译，并 `sudo make install` 安装

安装完成后可以单独使用 `colordiff -g` 命令来比较两个文件的差异，与 `diff` 命令参数一致

### 配置 svn

* 执行 `vim ~/.subversion/config` 编辑 `~/.subversion/config` 文件

* 将 `diff-cmd = diff_program` 的注释行，去掉注释并修改成 `diff-cmd = colordiff`，保存退出

之后执行 `svn diff` 命令的时候，就可以彩色化的显示版本差异了，其实这样配置，相当于在执行 `svn diff` 的时候多加了一个参数 `svn diff --diff-cmd = colordiff`