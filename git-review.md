1、git全局设置
	git config --global user.name "nazul"
	git config --global user.email "xxxx@xxxx.com"
2、初始化git仓库
	git init
	注：建议git中的文件使用标准的utf-8编码，如果食用notepad++作为文本编辑器，需要设置编码格式为utf-8 without bom。
3、基本操作
	git add filename	--添加文件到工作区（仓库）
	git commit -m “remark”	--提交文件到仓库中，并添加备注信息
	git status		--查看工作区和仓库状态，可以查看到未提交到工作区的文件以及添加到工作区，但是未提交到仓库中的文件。
	git diff filename	--文件对比
	git log 		--查看提交日志
	git log --pretty=oneline	--每次提交输出一行记录
	git reset --hard HEAD^	--回溯至上一个提交版本，注：HEAD表示当前版本，HEAD^表示上一版本，依次类推：上上版本为HEAD^^，可以使用提交时的版本id代替，id只需输入足以区分版本的位数即可。
	git reset --hard 5345234	--如上所述，回溯至某个版本
	git reflog		--查看执行的每个命令，可以作为查看版本id的工具
	git checkout -- filename	--放弃暂存区中该文件的修改，将文件恢复至仓库中的最后一版本。
 	git reset HEAD filename		--将提交到仓库的文件恢复到暂存区状态		git rm filename		--从版本库中删除文件，，然后用git commit提交
	ssh-keygen -t rsa -C "email.address"	--生成ssh密钥对，并将公钥添加到git官方平台中
	git remote add origin git@github.com:yanwu401909/learngit.git	--关联本地仓库和git线上仓库，远程仓库默认名为origin
	git push -u origin master	--将本地仓库推送到远程，即把当前分支master推送到远程，如果远程库时空的，第一次推送master分支时，添加-u参数，git不但会把本地master的分支推送到远程的新的master分支，还会把本地的master分支和远程master分支关联起来，在以后的推送过程中就可以简化命令
	git push origin master	--将本地的master分支推送到github
	git clone git@github.com:yanwu401909/gitskills.git	--克隆一个github上的库到本地

	
	
	
4、git已经提交到工作区的文件，在经过再次修改然后commit时，不会将最新的文件内容提交，只是将上次提交到暂存区的文件提交到仓库中。
