# Vim插件

手动安装 Vim 插件的方式以相当繁琐，Vundel 的诞生是大势所趋，不过内网机不能连外网，所以也就体会不太到使用 Vundel 的便捷，当然可以将插件的仓库拷贝到本地，再使用 Vundle 来安装管理。


## 插件清单

* ### Vundle

    Vim 插件管理器

* ### Vim airline

    逼格相当高的状态栏插件

* ### Vim fugitive

    状态栏显示 git 仓库状态
    
* ### Vim-colors-solarized

    solarized 颜色
    

* ### <a id="a">A</a>

    用于快速跳转 .h 和 .cpp 文件

    #### 功能键

    * 输入命令 `:A` 会跳转到对应的 .h 或 .cpp 文件

    * 输入命令 `:AV` 会垂直切割出新的窗口来打开对应的 .h 或 .cpp 文件

    * 输入命令 `:AS` 会水平切割出新的窗口来打开对应的 .h 或 .cpp 文件


* ### <a id="doxygen">Doxygen Toolkit</a>

    用于快速插入 Doxygen 注释。

    #### 功能键

    * 输入 `:Dox` 会在函数或类的定义的上一行插入 Doxygen 注释

    * 插入 `:DoxAuthor` 会在光标位置出插入 `文件名`，`作者`，`时间`等信息。
        
        
* ### <a id="echofunc">Echofunc</a>

    快速查看函数原型。


* ### <a>NERD Commenter</a>

    用于快速注释和取消注释代码行。

    #### 功能键：

    * `\` `c` `c` ：注释当前行或已选的代码块。
    * `\` `c` `c` ：与上面功能相反，取消注释。
    * `\` `c` `m` ：使用多行注释样式 `/* */` 注释。
	* `<number>` `\` `c` `c` ：注释<number>行


* ### <a id="omnicpp">OmniCppComplete</a>

    快速补全C++代码。

    #### 功能键

    * 输入 `.` 后自动补全成员函数/成员变量名

    * 输入 `->` 后自动补全成员函数/成员变量名

    * 输入 `::` 后自动补全类成员

    * `Ctrl` + `X` 随后 `Ctrl` + `X` 随后 `Ctrl` + `N` ：自动补全代码

    * `Ctrl` + `X` 随后 `Ctrl` + `X` 随后 `Ctrl` + `P` ：自动补全代码（反序选择）

    * `Ctrl` + `N` ：选择补全列表中的下一项或使用局部关键字补全代码

    * `Ctrl` + `P` ：选择补全列表中的上一项或使用局部关键字补全代码


* ### <a id="snipmate">SnipMate</a>

    代码补全插件。

    #### 功能键

    * 输入 `for` 然后按 `Tab` 会自动插入下面这些代码

    ```cpp
    for (i = 0; i < count; i++) {
        /* code */
    }
    ```

    然后再按 `Tab` 键，光标会依次跳转到模板代码中各个可编辑的值部分，以便修改成你想要的代码。

    可以自己新建或编辑对应的模板代码，以适应自己的编码风格，模板代码存放于 `~/.vim/snipmat/` 中。


* ### <a id="supertab">SuperTab</a>

    使用 `Tab` 键补全代码。

    #### 功能键

    * 输入部分关键字后按 `Tab` 会搜索局部作用域中的关键字去补全代码

    * 按 `Tab` 键会选择下一个补全列表中的选项



* ### <a id="taglist">TagList</a>

    代码结构化视图。

    #### 功能键

    * 输入 `:TlistToggle` 打开 Taglist。

    * 将光标移动到某个 tag 上，然后按 `空格` 键，在命令栏中会显示该tag在源码中完整的写法。

    * 将光标移动到某个tag 上，然后按 `回车` 键，会跳转到相应文件的定义出。


* ### vim-markdown

    markdown 语法高亮


* ### <a id="bookmarking">Bookmarking</a>

    用于标记你感兴趣的内容（书签）。

    #### 功能键

    * 输入命令 ` ：ToggleBookmark` 会在光标当前行创建一个书签

    * 输入命令 `:NextBookmark` ：会跳转到下一个书签位置处

    * 输入命令 `:PreviousBookmark` ：会跳转到上一个书签位置处


* ### VimIM

    输入法插件。

	```shell
	brew install berkeley-db
	sudo su -
	easy_install pip
	YES_I_HAVE_THE_RIGHT_TO_USE_THIS_BERKELEY_DB_VERSION=1 BERKELEYDB_DIR=/usr/local/Cellar/berkeley-db/6.1.26/ pip install --user bsddb3
	```


## 自定义快捷键

* ### `Ctrl` + `A`

    相当于执行 `:A`（[A 插件](#a) 的功能键），跳转到当前文件对应的 .h  或 .cpp 文件中，如果不存在则会询问是否建立。

* ### `Ctrl` + `A` 紧接着 `Ctrl` + `V`

    相当于执行 `:AV`，功能同上，但会再垂直切割出新的窗口来打开对应文件。

* ### `tt`

打开 [TagList 插件](#taglist)，相当于执行 `:TlistToggle`。

* ### `Tab`

[SuperTab](#supertab) 和 [snipMate](#snipmate) 插件的功能键，可以补全关键字和快速插入预定义的语法格式。

* ### `F5`

在当前行插入书签 （插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:ToggleBookmark`。

* ### `F6`

跳转到下一个书签（插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:NextBookmark`。

* ### `F7`

跳转到上一个书签（插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:PreviousBookmark`。
