插件追踪
热键追踪
个性化追踪

git

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

gitgutter

	需配置git 环境变量 只需到外层父目录即可
	需要电脑性能，有卡顿 无良好体验
