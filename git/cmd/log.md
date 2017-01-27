# git log

`git log` ：显示 `<commit-id>`，`<author>`，`<author-date>`，和 `<msg>`。

`git log --pretty=oneline` ：单行log，显示 `<commit-id>` 和 `<msg>`。  
`git log --pretty=short` ：显示 `<commit-id>`，`<author>` 和 `<msg>`。  
`git log --pretty=medium` ：默认值，相当于 `git log`，显示 `<commit-id>`，`<author>`，`<author-date>`，和 `<msg>`。
`git log --pretty=full` ：显示 `<commit-id>`，`<author>`，`<commit>` 和 `<msg>`。  
`git log --pretty=fuller` ：显示 `<commit-id>`，`<author>`，`<author-date`>，`<commit>`，`<commit-date>`，和 `<msg>`。
`git log --pretty=email` ：显示 `<commit-id>`，`<from>`，`<date`>，和 `<subject>`。
`git log --pretty=raw` ：显示 `<commit-id>`，`<tree>`，`<parent>`，`<author + raw-time>`，`<committer + raw-time>`，和 `<msg>`。

`git log -<number>`  
`git log -n <number>`  
`git log --max-count=<number>`

`git log --graph` ：分支合并图。


`git log --abbrev-commit` ：显示简短的 `<commit_id>`。

`git log -p`  
`git log -u`  
`git log --patch` ：生成补丁，显示此次提交与上次版本的差异。

`git log --stat` ：生成差异状态(diffstat)，显示文件修改的统计信息。

`git log --shortstat` ：只显示 `--stat` 中最后的行数修改、添加、移除统计。

`git log --name-only` ：仅显示已修改文件的名字。

`git log --name-status` ：显示已修改文件的名字和状态。

`git log --relative-date` ：使用较短的相对时间（例如：2 weeks age）。
