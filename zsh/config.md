# 配置 zsh

* 修改主题为 *agnoster*

    * 执行 `vim ~/.zshrc 编辑` *zsh* 配置

    * 将 `ZSH_THEME` 的值改成 `agnoster`

    * 在文件尾部添加 `export DEFAULT="your_name"，`your_name` 是终端登录用户的全称，可以执行 `whoami` 查看

    * 在文件尾部添加下面这些配置

    ```shell
    export DEFAULT_USER=your_name
    export CLICOLOR=1
    export LSCOLORS=gxfxaxdxcxegedabagacad
    export LANG=zh_CN.UTF-8

    alias ls="ls -FhOT"
    alias ll="ls -lFhOT"
    alias la="ls -laFhOT"
    alias rm="rm -i"
    alias cp="cp -i"
    alias mv="mv -i"
    alias mkdir="mkdir -v"
    ```

    将上面配置中的 `your_name` 替换成你登录终端使用的用户名，可以使用 `whoami` 命令查看。

    * 修改终端字体为 *Inconsolata for Powline*

    具体参考 [iTerm修改字体](../iterm2/preference.md) 章节
