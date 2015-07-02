# 让 vim 飞


完善了一下开发机（192.168.180.15）上 vim 的配置，具体总结如下。想要使用一样的配置的话，可以使用 root 帐号登录开发机器，然后将 `/home/shenyu/.vim` 和 `/home/shenyu/.vimrc` 拷贝到自己的 `/home/yourname` 目录下。


## 自定义快捷键

* ### `Ctrl` + `A`

    相当于执行 `:A`（[A 插件](#a) 的功能键），跳转到当前文件对应的 .h  或 .cpp 文件中，如果不存在则会询问是否建立。


* ### `Ctrl` + `A` 紧接着 `Ctrl` + `V`

    相当于执行 `:AV`，功能同上，但会再垂直切割新的窗口来打开对应文件。


* ### `F2`

打开 [TagList 插件](#taglist)，相当于执行 `:TlistToggle`。


* ### `F3`

打开 [NERDTree 插件](#nerdtree)，相当于执行 `:NERDTreeToggle`。


* ### `F4`

折叠代码块，相当于执行 `z` `a`。


* ### `F5`

在当前行插入书签 （插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:ToggleBookmark`。


* ### `F6`

跳转到下一个书签（插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:NextBookmark`。


* ### `F7`

跳转到上一个书签（插件 [Bookmarking](#bookmarking) 的功能键），相当于执行 `:PreviousBookmark`。


* ### `F8`

取消搜索结果的高亮，相当于执行 `:nohlsearch`。


* ### `F9`

高亮文中所有匹配光标位置所指的单词，并输入全文替换的命令。


* ### `Tab`

[SuperTab](#supertab) 和 [snipMate](#snipmate) 插件的功能键，可以补全关键字和快速插入预定义的语法格式。



## 插件列表

* ### <a id="a">A</a>

    用于快速跳转 .h 和 .cpp 文件。


* ### <a id="bookmarking">Bookmarking</a>

    用于标记你感兴趣的内容（书签）。


* ### <a id="doxygen">Doxygen Toolkit</a>

    用于快速插入 Doxygen 注释。

    * 功能键

        * 输入 `:Dox` 会在函数或类


* ### <a id="nerdtree">NERDTree</a>

    目录树插件。

    * ####功能键：
        * 输入 `:NERDTreeToggle` 打开 NERDTree


* ### <a>NERD Commenter</a>

    用于快速注释和取消注释代码行。

    * ####功能键：

        * `\` `c` `c` ：注释当前行或已选的代码块。

        * `\` `c` `c` ：与上面功能相反，取消注释。

        * `\` `c` `m` ：使用多行注释样式 `/* */` 注释。


* ### <a id="omnicpp">OmniCppComplete</a>

    快速补全C++代码。


* ### <a id="snipmate">SnipMate</a>

    代码补全插件。


* ### <a id="supertab">SuperTab</a>

    使用 `Tab` 键补全代码。


* ### <a id="taglist">TagList</a>

    代码结构化视图。

    * #### 功能键

        * 输入 `:TlistToggle` 打开 Taglist。

        * 将光标移动到某个 tag 上，然后按 `空格` 键，在命令栏中会显示该tag在源码中完整的写法。

        * 将光标移动到某个tag 上，然后按 `回车` 键，会跳转到相应文件的定义出。





