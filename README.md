同步本仓库使用Package Control 进行插件自动安装前装备工作

	nodeJs http://nodejs.cn/ 或者 https://nodejs.org/en/
	ruby http://rubyinstaller.org/downloads/
	compass 使用控制台指令 gem install compass
	TortoiseSVN https://tortoisesvn.net/
	git https://git-scm.com/download/

插件追踪 {Package Control.sublime-settings}
热键追踪 {Default (Windows).sublime-keymap}

个性化追踪 {Preferences.sublime-settings}
Autoprefixer {Autoprefixer.sublime-settings}
Snippets

	{
		文件名规则:CH-快捷键,
		htmlf:新建html5文档模板,
	}

Git 版本管理工具

	前往 https://git-scm.com/download/ 下载安装程序，安装完成后即可开始使用

	壹
		git init 初始化仓库
		git add all |git add .
		git commit |git commit -m "commit msg"
		git remote
			remote -v	远端仓库
			remote add origin url 添加
			remote remove origin 移除
		git push	推送
			push --upstream origin master 首次添加远端仓库推送关联
		git pull

	贰

		git clone url
		git add all	|git add .
		git commit |git commit -m "commit msg"
		git push
		git pull

	版本回退
		git log |git reflog
		git reset --hard {	HEAD | HEAD^ | HEAD@{Num}	}

Sublimegit 插件使用

	欲正常使用需要使用ssh协议进行验证身份推送
	添加ssh
		git config --global user.name<user.email>
		ssh-keygen -t rsa -C "example@example.com"
	如果已存在这覆盖掉
		eval "$(ssh-agent -s)"
	ssh-add ~/.ssh/id_rsa(ssh私钥名称)
		添加公钥到github
	测试ssh
		ssh -T git@github.com
		你将会看到：
		
		    The authenticity of host 'github.com (207.97.227.239)' can't be established.
		    RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
		    Are you sure you want to continue connecting (yes/no)?
		选择 yes
		Hi humingx! You've successfully authenticated, but GitHub does not provide shell access.
		如果看到Hi后面是你的用户名，就说明成功了。
	至此可集成在Sublime 中完成提交推送

TortoiseSVN

	安装本插件需要先安装window版本SVN小乌龟 (TortoiseSVN)
	完成后安装本插件 只需注意小乌龟的路径即可使用本插件正常调用小乌龟进行提交更新等操作

gitgutter

	需配置git 环境变量 只需到外层父目录即可
	需要电脑性能，有卡顿 无良好体验


Sass css预处理

	简介 使用Sass需要ruby环境，前往 http://rubyinstaller.org/downloads/ 下载最新安装包，
		安装后进入系统控制台程序(cmd/shell)
		安装compass	{gem install compass/sudo gem install compass}
		更换源地址(http://gems.ruby-china.org/) 更新ruby：gem update --system
		期间各种安装错误，可尝试使用代理[参考 http://gems.ruby-china.org/]
		总站地址 ruby中国 http://ruby-china.org/

	安装sass http://www.sasschina.com/install/
	安装sublime插件[sass,sass-build,sass-snippets]
	使用指导 参考 http://www.sasschina.com/guide/
