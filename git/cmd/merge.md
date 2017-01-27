# git merge

`git merge <branchname>` ：合并 `<branchname>` 至当前分支，默认以 `fast-forward` 方式合并，不会产生对应的 `commit`

`git merge -ff <branchname>` ：以 `fast-forward` 方式合并 `<branchname>` 至当前分支，这是默认的合并方式（同上）

`git merge -no-ff <branchname> -m <msg>` ：不以 `fast-forward` 方式合并 `<branchname>` 至当前分支，会产生对应的 `commit`，这是合并带注释信息标（annotated tag）的默认方式

`git merge -no-ff <branchname>` ：不以 `fast-forward` 方式合并 `<branchname>` 至当前分支，会产生对应的 `commit`，没有指定 `-m` 参数，执行后需要在执行 `git commit -m <msg>` 来完成本次合并操作
