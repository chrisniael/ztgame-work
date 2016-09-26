# vim-airline

Vim 状态栏插件，要设置状态栏主题，请配合安装插件 [vim-airline-themes](vim-airline-themes.md)

![vim-airline](https://raw.githubusercontent.com/chrisniael/vim-configuration/master/images/vim-airline.gif)

## 安装

* Vundle

    ```vim
    Plugin 'vim-airline/vim-airline`
    ```

## 配置

```vim
set t_Co=256       " Explicitly tell Vim that the terminal supports 256 colors
set laststatus=2
let g:airline_powerline_fonts=1
let g:airline#extensions#tabline#enabled=1    " enable tabline
let g:airline#extensions#tabline#buffer_nr_show=1    " 显示buffer行号
let g:airline_theme="solarized"
"set ambiwidth=double    " When iTerm set double-width characters, set it
```
