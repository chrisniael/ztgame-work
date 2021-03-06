# 偏好设置

* 快捷键设置 (Keys)

	![Keys](img/keys.png)

	* `Preferences` -- `Keys`，勾选 `Show/hide iTerm2 with a system-wide hotkey`

* 外观设置 (Appearance)

	![Appearance](img/appearance.png)

	* 不隐藏标签页数字

		`Preferences` -- `Appearance`，取消勾选 `Hide tab number and tab close button`

	* 不显示窗口序号

		`Preferences` -- `Appearance`，取消勾选 `Show window number`

	* 隐藏标签页活动指示器

		`Preferences` -- `Appearance`，勾选 `Hide tab activity indicator`
		
* Profiles
		
	* 无限回滚

		![Terminal](img/profile-terminal.png)
		
		`Preferences` -- `Profiles` -- `Terminal`，勾选 `Unlimited scrollback`
	
	* 使用 *Solarized* 主题
	
		![Theme](img/theme.png)
	
		* 安装 *Solarized* 主题
	
		* `git clone https://github.com/altercation/solarized.git`
		
			* 在 *Finder* 中打开目录 `solarized/iterm2-colors-solarized`
	
			* 双击 `Solarized Dark.itermcolors` 安装 *Solarized* 主题至 *iTerm*
	
			* `Preferences` -- `Profiles` -- `Colors`，点击 `Load Presets`，选中 `Solarized Dark`
	
	* 非ASCII字体设置为 *Inconsolata for Powerline*
		
		![font](img/font.png)
	
		这个字体的设置和 *Oh My Zsh* 的 `angoster` 主题以及 *Vim* 的 `airline` 插件有关
	
		* 安装 *Powerline* 字体
			
			* `git clone https://github.com/powerline/fonts.git`
			
			* `cd font`
			
			* `./install.sh` （取保又执行权限）
	
		* `Preferences` -- `Profiles` -- `Text`，点击在 `Non-ASCII Font` 栏的 `Change Font`，选中 `Inconsolata for Powerline` 字体


