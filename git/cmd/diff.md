# git diff

`git diff` ：比较 `Working Directory` 与 `Stage` 中所有文件的变化，仅仅会比较 `Stage` 与 `Working Directory` 中都存在的文件，就是说，某个文件未被 `Tracked` 进 `Stage` 的话，是不会进行比较的。

`git diff <file>` ：比较 `Working Directory` 与 `Stage` 中 `<file>` 文件的不同，仅仅会比较 `Stage` 与 `Working Directory` 中都存在的文件，就是说，某个文件未被 `Tracked` 进 `Stage` 的话，是不会进行比较的。

`git diff HEAD <file>` ：比较 `Index` 与 `Stage` 中 `<file>` 文件的不同。

`git diff -p <commit> <commit>`  
`git diff -u <commit> <commit>`  
`git diff --patch <commit> <commit>` ：生成两次提交的差异补丁。

`git diff --cached`  
`git diff --staged` ：比较 `Stage` 与 `Index` 中文件的变化。

`git diff <file>` ：比较 `Working Directory` 与 `Stage` 中 `<file>` 文件的变化，仅仅会比较 `Stage` 与 `Working Directory` 中都存在的文件，就是说，某个文件未被 `Tracked` 进 `Stage` 的话，是不会进行比较的。
