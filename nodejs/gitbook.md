# GitBook

## 安装 GitBook

* Mac

	* 安装 node.js

		下载地址：[https://nodejs.org/en/download/](https://nodejs.org/en/download/)，点击 `Macintosh Installer (.pkg)`，下载 pkg 安装包，下载完>后，打开，会自动安装到相应路径中

	* 修改 npm 镜像源

		```shell
		npm config set registry https://registry.npm.taobao.org
		```

	* 安装 GitBook

		```shell
		sudo npm install -g gitbook-cli
		sudo gitbook versions:install latest
		```
		耐心等一会儿

	* 安装 Calibre for Mac

		下载地址：[http://calibre-ebook.com/download](http://calibre-ebook.com/download)

	* 安装 ebook-convert

		改组件用于生成pdf，mobi，epub格式的电子书，集成在 Calibre 中

		```shell
		sudo ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
		```
