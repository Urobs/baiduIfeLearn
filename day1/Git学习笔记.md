# Git学习笔记

## 创建版本库

`git init //初始化git版本库`

`git add <file> //添加文件到暂存区`

`git commit -m <message> //提交文件`

## 版本控制

`git status //查看工作区状态`

`git diff // 查看修改内容`

**版本指针HEAD**

![版本指针](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907584977fc9d4b96c99f4b5f8e448fbd8589d0b2000/0)

`git reset --hard commit_id // 版本穿梭`

`git reser --hard HEAD^ // 上个版本(HEAD^^上上个版本)`

`git log // 查看提交历史`

`git reflog // 查看命令历史`

**工作区和版本库**

![工作区和版本库](https://cdn.liaoxuefeng.com/cdn/files/attachments/001384907720458e56751df1c474485b697575073c40ae9000/0)

版本库分为stage（暂存区）和 master分支

`git add` 提交到暂存区， `git commit` 提交到版本库

`git checkout -- file // 丢弃工作区的修改`

`git reset HEAD <file>`

## 远程库

push到GitHub仓库我遇到的小问题是使用的Windows Ubuntu子系统的git并没有pub ssh key与GitHub相关联，而我习惯性地认为两者是相关联的。

## 分支

`git checkout -b dev // 创建dev分支`

`git branch <name> // 查看分支`

`git checkout <name> // 切换分支`

`Fast-forward 模式即直接把master指向dev，所以很快`

`git merge <name> // 合并某分支到当前分支`

`git branch -d <name>  // 删除分支`