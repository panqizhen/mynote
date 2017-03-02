有关git的命令
git init//初始化，将会创建一个.git文件夹
git remote add origin https://github.com/panqizhen/mynote.git//创建分支
git pull origin master///相当于y远程获取最新版本并合并
git push origin master//本地推送到远程
git push -u origin master//本地推送到远程，用于初始化
相当于git fetch origin master:tmp
git diff tmp
git merge tmp
git config --global credential.helper wincred//将登陆信息保存在本地
git clone https://github.com/panqizhen/mynote.git//直接从远程克隆就不需要配置了
git remote rm origin//删除来源
在文件config
[branch "master"]
	remote = origin
	merge = refs/heads/master
表示分支
git可以

