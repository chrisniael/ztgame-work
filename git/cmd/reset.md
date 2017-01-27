# git reset

`git reset --hard <commit_id>` ：退回到 `<commit_id>` 这个版本。


`git reset --hard HEAD^` ：退回到 `HEAD` 所指版本的上一版本

HEAD : 当前版本  
HEAD^ : 当前版本的 `上` 个版本  
HEAD^^ : 当前前版本的 `上上` 个版本  
HEAD^^^ : 当前版本的 `上上上` 个版本  
.  
.  
.

HEAD~1 : 当前版本的 `上` 个版本库  
HEAD~2 : 当前版本的 `上上` 个版本  
HEAD~3 : 当前版本的 `上上上` 个版本  
.  
.  
.


`git reset HEAD <file>` ：将 `Stage` 中 `<file>` 文件的状态恢复至 `HEAD` 指向的版本中 `<file>` 的状态。
