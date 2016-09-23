# Vundle

Vundle 是 Vim 的插件管理器，相当好用。

## 安装 Vundle

* 使用 Git clone Vundle 的代码至 `~/.vim/bundle/Vundle.vim` 目录中

    ```shell
    git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
    ```

* 打开 Vim 配置文件 `~/.vimrc` ，将下面这些配置信息写入进去（保持这些配置在最上面，否则会>有问题）

    ```vim
    set nocompatible              " be iMproved, required
    filetype off                  " required

    " set the runtime path to include Vundle and initialize
    set rtp+=~/.vim/bundle/Vundle.vim
    call vundle#begin()

    " let Vundle manage Vundle, required
    Plugin 'gmarik/Vundle.vim'
    " The following are examples of different formats supported.
    " Keep Plugin commands between vundle#begin/end.
    " plugin on GitHub repo
    Plugin 'tpope/vim-fugitive'

    " All of your Plugins must be added before the following line
    call vundle#end()            " required
    filetype plugin indent on    " required
    ```

## 安装 Vim 插件

* 添加插件至 `~/.vimrc`，放在 `Plugin 'gmarik/Vundle.vim'` 之后

    ```vim
    " let Vundle manage Vundle, required
    Plugin 'gmarik/Vundle.vim'
    " The following are examples of different formats supported.
    " Keep Plugin commands between vundle#begin/end.
    " plugin on GitHub repo
    Plugin 'tpope/vim-fugitive'
    ```

* 打开 Vim，执行 `:BundleInstall` 命令安装所有的插件（耐心等一会儿）
