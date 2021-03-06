﻿初始化仓库：
    git init

提交代码：
    git add 修改的文件
    git add 文件1 文件2 ...(多个文件用空格隔开)
    git commit -m "备注"

检查仓库状态：
    git status

检查文件修改：
    git diff 文件名

查看提交日志：
    git log
    git log --pretty=oneline(显示成一行)

版本回退：
    git reset --hard 版本号

查看历史命令：
    git reflog

查看工作区和版本库的区别：
    git diff HEAD -- 文件名

撤销工作区修改：
    git checkout -- 文件名 （撤销到最后一次add/commit的状态，也可以找回工作区删除的文件）

撤销暂存区修改：
    git reset HEAD 文件名

删除文件：
    git rm 文件名 （更改到暂存区）

关联到远程仓库：
    git remote add origin git@github.com:6654cui/learningGit.git
    
推送远程仓库：
    git push -u origin master （初次提交加上 -u 关联本地和远程仓库）
    git push origin master

克隆远程仓库：
    git clone git@github.com:6654cui/study-Plan.git

创建分支：
    git checkout -b 分支名
    相当于：
    git branch dev
    git checkout dev (切换分支)

合并分支：
    1.切换至目的分支
    2.合并分支
        git merge dev

删除分支：
    git branch -d 分支名

查看分支合并情况：
    git log --graph --pretty=oneline --abbrev-commit

不使用Fast forwad方式合并分支
    git merge --no-ff -m "备注内容" 分支名

从远程仓库拉取：
    git pull origin master

创建标签
    git tag <name>

查看标签
    git tag

查看远程仓库地址
    git remote -v

查看最新的commit
    git show

查看指定commit hashID的所有修改：
    git show commitId
    
查看某次commit中具体某个文件的修改：
    git show commitId fileName