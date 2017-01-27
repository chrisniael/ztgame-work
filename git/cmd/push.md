# git push

`git push` ：推送所有的分支。

`git push <remote> <local_branch>` ：推送 `<local_branch>` 分支至 `<remote>` 仓库中同名的分支中，如果 `<remote>` 中的 `<local_branch>` 分支不存在，则建立同名的远程分支。

`git push -u <remote> <local_branch>` ：推送 `<local_branch>`  分支至 `<remote>` 仓库中同名的分支中，如果 `<remote>` 中的 `<local_branch>` 分支不存在，则建立同名的远程分支，并将本地分支 `<local_branch>` 关联到远程分支上

`git push <remote> <local_branch>:<remote_branch>`

`git push <remote> :<remote_branch>` ：仅仅删除远程分支 `<remote_branch>` ,  如果要删除本地分支，使用 `git branch -d <local_branch>`
