# git tag

`git tag` ：查看所有标签

`git tag <tagname>` ：新建标签 `<tagname>`，指向 `HEAD`

`git tag -a <tagname> -m <msg>` ：新建一个未签名的（unsigned），带注释的（annotated）标签 `<tagname>`，指向 `HEAD`

`git tag -s <tagname> -m <msg>` ：新建一个使用 `GPG` 签名的标签 `<tagname>`，using the default email address's key.

`git tag -d <tagname>` ：删除本地标签 `<tagname>`

`git push origin <tagname>` ：推送本地标签 `<tagname>` 至远程仓库

`git push origin --tags` ：推动所有本地未推送过的标签至远程仓库

`git push origin :refs/tags/<tagname>` ：删除远程标签 `<tagname>`
