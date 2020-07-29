# Git学习

## Git安装

## 初始化Git仓储（/仓库）
- 这个仓库会存放，git对我们的项目代码进行备份的文件
- 在这个项目右键打开 git bush
- 初始化命令“git init”

## 配置个人信息
- 在git中配置当前使用的用户是谁
- 命令： 
 + $ git config --global user.name "evan"
 + $ git config --global user.email "928946604@qq.com"
 
## 将代码放置到git仓库
- 1、预添加 
	+ $ git add ./目录路径（或文件全名）
- 2、提交代码  
	+ $ git commit -m "本次提交改变说明"
 
## 命令查看状态
- git status
	+ modified（绿色）：表示已经放置到暂存区域  即已经执行add
	+ modified（红色）：已修改文件但是未执行任何指令

## 添加多个文件
- git add ./    //将当前的所有文件都提交

## 一次性提交（不用分为add和commit操作）
- git commit --all -m “一次性操作” //把所有修改过的代码放置到git中


## 查看所有提交日志记录
- git log
- git log --oneline 查看精简日志信息

## 版本回退
- 先通过日志查看备份记录
- 命令： git reset --hard Head~0  //Head~0代表的是最新的一个备份
- 根据版本号回退（指定版本）
	+ git reset --hard 版本号（提交时的唯一标识）
## 查看回退后被覆盖的版本号
- git reflog   //可以看到查看切换版本的记录

## 分支
### 分支提交（功能开发未完善的代码提交方式）
- git branch 分支名称    //创建分支
- git branch 			 //查看所有分支
 + "*"表示当前所在的分支
- git checkout 分支名称  //切换到其他分支
### 合并分支
- git merge 分支名称

## 上传到云服务器    GitHub
- git push [地址] 分支名称
  + 例： git push https://github.com/Evan1979/AuroraCloud.git master
 
## 从云服务器下载源码到本地
- git pull  https://github.com/Evan1979/AuroraCloud.git master
  （*记得先初始化一个git仓储   git init!*）

## 克隆项目
- git clone [地址](*一般是第一次使用!，多次执行会覆盖本地目录内容*)


## ssh方式提交
- 原理： 公钥和私钥
- 生成公钥 私钥
	+ ssh-keygen -t rsa -C "邮箱"
- 命令 ： git push git@github.com:Evan1979/sshTest.git master
	
- 不需要输入用户名及时就可以上传源码
- git@github.com:Evan1979/AuroraCloud.git
- git@github.com:Evan1979/sshTest.git

- 多人开发   更新代码
	+ 命令： git pull git@github.com:Evan1979/sshTest.git master

## 
## 
## 
## 
 