 ## 版本控制系统
 #本地
 缺点：容易丢失
 #集中化
 缺点：
	不支持离线提交
	依赖版本数据库
	代表：SVN
 #分布式
 优点：
	支持多人协作开发
	可以使用任何客户端的备份进行恢复
	
###git
##优点
	1：记录快照（没有修改则保留链接指向之前存储的文件），而非差异存储。
	2：断网后依然可以进行版本管理
##缺点
	占用磁盘空间大
#git的3个区域：工作区，暂存区，git仓库
#git的3个状态：已修改，已暂存，已提交
#工作区文件的4个状态:未被git管理为未跟踪，加git的3个状态

##相关命令
1:配置用户名		
git config --global user.name "csx"  
2:邮箱地址		
git config --global user.email "1814254847@qq.com"
（配置文件存放在C:\Users\Administrator\.gitconfig中）
3:查看所有全局配置项
git config --list --global
4：查看指定配置项
git config --global user.name
5：获取帮助信息
git help <verb>
6:获取config命令帮助手册
git help config
7:获取快速参照
git help -h

#创建git仓库
git init

#检查文件状态
git status
#以精简的方式显示文件状态
git status -s
git status --short
#跟踪文件,把已跟踪且已修改的文件放到暂存区
git add <filename>
#提交更新,把暂存区的文件提交到git仓库
git commit -m "提交信息"
#撤销对文件的修改
git checkout -- <filename>
#将所有文件加入暂存区
git add .
#移除暂存的文件
git reset HEAD <filename>
#跳过暂存，直接提交
git commit -a -m "描述信息"
#同时移除工作区和git仓库中的文件
git rm -f <filename>
