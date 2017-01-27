# git config

`git config --global user.name "shenyu"`

`git config --global user.email "shenyu@shenyu.me"`

`git config --global credential.helper cache` ：配置到缓存，默认15min（未玩过）


`git config --global credential.helper 'cache --timeout=3600'` ：修改缓存时间（没玩过）


```shell
git config --global color.ui auto
git config --global color.status auto
git config --global color.branch auto
git config --global color.diff auto
git config --global color.grep auto
git config --global color.interactive auto
```

```shell
git config --global alias.co checkout
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.br branch
```
设置命令的别名

`git config --global core.editor vim` ：设置编辑器使用 `vim`


`git config -l`  
`git config --list` ：`list` 所有配置


用户配置文件位置：`~/.gitconfig`，以上命令执行后，都会将配置内容记录在这个文件中。
