# git checkout

`git checkout -- <file>` ：从 `Stage` 中检出 `<file>` 覆盖 `Working Directory` 中的 `<file>` 中的文件，前提是 `<file>` 已经 `Tracked` 在 `Stage` 中了。（当你在 `Working Directory` 中修改完文件后，想要恢复修改之前的状态，可以这么玩）

`git checkout <branch>`

`git checkout -b <branch>` ：`<branch>` 分支如果不存在新建 `<branch>` 分支，并切换到 `<branch>` 分支处；`<branch>` 分支如果已经存在，则直接切换到 `<branch>` 分支。
