# CentOS Home目录下中文路径转中文

Home 目录下文件夹是中文的话，命令行操作起来相当麻烦。


```shell
export LANG=en_US
xdg-user-dirs-gtk-update
```

执行完上面的设置后，会弹出一个窗口，选择确认，然后再将环境变量 `LANG` 改回来

```shell
export LANG=zh_CN.UTF-8
``
