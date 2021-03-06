

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

当分支都存在新的提交时，就会产生冲突，无法执行Fast-forward模式，必须手动解决冲突

`git log --graph // 查看分支合并图`

`git merge --no-ff -m "merge with no-ff" dev // --no-ff表示禁用Fast forward, 如果是F f模式因为是直接将master指针指向dev，因此删除dev后会丢失分支信息，而禁用Ff提交一个新的commit，会保留分支信息`

`git stash  // 储存当前工作区`

`git stash list // 列出当前储存的工作区`

`git stash pop // 恢复并删除储存的工作区`

`git stash apply // 恢复储存的工作区`

`git stash drop // 删除储存的工作区`

开发一个新功能使用feature分支

`git branch -D <name> // 强行删除没有被合并的分支`

多人协作工作模式

`git push origin <branch name> // 推送自己的修改`

`git checkout -b deb origin/dev // 创建远程dev分支到本地`

`如果远程推送失败，则意味着远程分支比你的更新，先使用git pull 试图合并；`

`如果合并有冲突， 先解决冲突，再在本地提交`

`解决冲突后，在 git push origin <branch name>`

`git rebase // 变基，将一系列提交按照原有次序应用到另一分支上，即为把原来未提交分的分支的提交历史合并成为一条直线 原则是只对未提交的本体修改执行变基操作清理历史，不对推送给别处的历史执行变基操作`

`tag和commit绑定在一起,使commit更容易记`

`git tag <tagname> // 新建一个标签，标签总是和commit挂钩,默认为HEAD，也可以指定一个commit号`

`git tag  // 查看所有标签信息`

`git tag -a <tagname> -m "xxx" // 指定标签信息`

`git show <tagname> // 查看标签信息`

`git tag -d <tagname> // 删除本地标签`

标签在默认情况下只存在于本地，需另外推送到远程

`git push origin  <tagname> // 推送标签到远程`

`git push  origin --tags // 推送全部标签`

`git push origin :refs/tags/<tagname> // 删除远程标签`

变基操作

1. 与merge操作的区别：merge为三方比对（两个分支的最近快照和最近的共同祖先），然后生成一个新的快照。而rebase为提取当前分支的所有修改到C3上。
2. 两者生成的最终结果所指向的快照是相同的

图解分析

![分支](https://git-scm.com/book/en/v2/images/basic-rebase-1.png)

如果使用merge:

`git checkout master`

`git merge experiment`

那么

![merge](https://git-scm.com/book/en/v2/images/basic-rebase-2.png)

rebase:

`git checkout experiment // 切换到experiment分支`

`git rebase master // 变基 实际上是把c4的修改添加c3生成一个新的快照C4^ 此时当前分支仍然是exp`

`git checkout master // 切换到主分支`

`git merge experiment // 合并分支` 

![变基](https://git-scm.com/book/en/v2/images/basic-rebase-3.png)



## 自定义git

`.gitignore文件的里面的后缀名，不提交到版本库`

`git config --global alias.st status //全局配置别名，此例表示st为 status`

`git config --global alias.cm "commit -m" // cm表示 commit -m `

`git config --global alias.br branch // global 为全局参数，意味着命令在这台电脑上的所有git仓库下都可以使用`

**配置文件**

`仓库的配置文件放在.git/config文件中， 而用户的配置文件放在用户的主目录的一个隐藏文件.gitconfig中`



