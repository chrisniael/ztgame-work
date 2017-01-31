# GitHub

GitHub 上有很多开源项目，要使用的话，需要先将自己的公钥添加到 GitHub 上。


* 生成 *SSH* 密钥

    * 执行 `ls ~/.ssh/` 查看 `~/.ssh/` 目录下是否存在 `id_rsa.pub` 和 `id_rsa` 文件，如果有的话>，就不需要再生成了

    * 执行 `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"` 生成密钥文件（将 `your_email@example.com` 替换成你自己的邮箱，然后会提示你一些东西，不用管，一直回车，就OK


* 添加 *SSH* 公钥至 *GitHub*

    * 执行 `pbcopy < ~/.ssh/id_rsa.pub` 将公钥文件 `id_rsa.pub` 的内容拷贝到剪切板

    * 登录 [GitHub](https://github.com)

    * 进入 `Setting`，点击左侧面板中的 `SSH keys`

    * 点击右上角 `Add SSH key`，将剪切板中的 *SSH公钥* 粘贴到 `key` 中，再填写一个你喜欢的 `title` 保存（点下面的 **Add key** 按钮）就OK了
