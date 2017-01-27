# git commit

`git commit -m <msg>`

`git commit -a -m <msg>` ：直接将已经被 `Tracked` 文件的改动（修改和删除）提交至 `Index` 中，不经过 `Staged`。

`git commit --amend` ：修改最后一次提交的内容和信息，将 `Stage` 中的文件重新提交。

`git commit -v` ：在提交信息的底部显示 `HEAD` 和将要提交之间的 `unifed diff`。注意这个 `diff` 的输出没有行前缀 `#` 。

`git commit -a -m <msg>` ：直接略过 `Stage` ，提交所有已经 `Tracked` 文件至 `Index`，相当于先 `add -u`，然后再 `commit -m`。
