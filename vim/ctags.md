# Ctags

Vim 很多插件需要用到 Ctags，例如代码补全的插件。

## 包管理器安装 Ctags

* Mac

    Mac 自带的 Ctags 并非我们需要的 Ctags，只是名字相同罢了，这里用 [Homebrew](http://brew.sh) 来安装 Ctags

    ```shell
    brew install ctags
    ```

* CentOS/RedHat

    ```shell
    sudo yum install ctags
    ```


## 源码安装 Ctags

* [下载](http://ctags.sourceforge.net/) 最新的 Ctags 源码，目前最新版本是 *5.8*（2009年7月9日发布，这么久没有更新了）

    ```shell
    wget http://prdownloads.sourceforge.net/ctags/ctags-5.8.tar.gz
    ```

* 解压 `ctags-5.8.tar.gz`

    ```shell
    tar -zxvf ctags-5.8.tar.gz
    ```

* 编译并安装 Ctags

    ```shell
    cd ctags
    make
    sudo make install
    ```
