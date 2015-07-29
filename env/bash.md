# bash

### bash 配置

在 `~/.bashrc` 或者 `~/.bash_profile` 中添加下面这些配置

```
alias rm='rm -i'
alias cp='cp -i'
alias mv='mv -i'
alias mkdir='mkdir -v'

alias ls='ls -Fh --color'
alias ll='ls -lFh --color'
alias la='ls -laFh --color'

#export PS1="\[\e[0;32m\][\[\e[0;31m\]\u\[\e[0;36m\]@\[\e[0;33m\]\h\[\e[0;34m\]:\[\e[0;35m\]\w\[\e[0;32m\]] \[\e[0;37m\]$ \[\e[0m\]
export PS1="\[\e[0;35m\]\w \[\e[0;37m\]$ \[\e[0m\]"

if [ -f /etc/bash_completion.d/subversion ]
then
    source /etc/bash_completion.d/subversion
fi
```