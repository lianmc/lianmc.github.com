---
layout: post
title: "读书笔记:Git权威指南"
date: 2012-10-13 10:28
comments: true
categories: [读书笔记, Git]
---
## Git初始化
#### 命令补全

	$ brew install bash-completion
	# add the following lines to your ~/.bash_profile
	if [ -f `brew --prefix`/etc/bash_completion ]; then
    	. `brew --prefix`/etc/bash_completion
	fi
	
#### 用户配置文件`~/.gitconfig`，系统配置文件`/etc/gitconfig`。

	$ git config --global user.name "xx"
	$ git config --global user.email "xx@mail.com"
	$ git config --system alias.ci commit
	$ git config --global color.ui true
	
#### 重新修改最新的提交
	$ git commit --amend -m "new message"
	
## Git暂存区(stage)
#### 查看提交日志
	$ git log --pretty=oneline

> 文件.git/index实际上就是一个包含文件索引的目录树，记录了文件名和文件在状态信息(时间戳和文件长度等)。文件的内容并没有存储在其中，而是保存在Git对象库.git/objects目录中，文件索引建立了文件和对象库中对象实体之间的对应。

#### 查看HEAD指向的目录树
	$ git ls-tree -l HEAD
#### git diff命令
* 工作区和暂存区比较`$ git diff`
* 暂存区和HEAD比较`$ git diff --cached`
* 工作区和HEAD比较`$ git diff HEAD`

> 不要使用git commit -a命令，减少用git add命令标识变更文件的步骤，会丢掉git暂存区带给用户的最大好处。
#### 保存当前工作进度
	$ git stash

## git 对象
git库中的objects目录说明：ID的前2位作为目录名，后38位作为文件名。

blob: binary large object, basic large object

## git 重置


	


	
	


