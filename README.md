# 基本概念
- 工作区
- 缓冲区
- 归档区

## 基本流程
1. git init：将当前工作目录初始化为仓库
2. git add 文件路径：将文件添加到缓冲区
3. git commit -m "注释信息"：将缓冲区提交到归档区
4. 添加到远端的仓库
    - git remote add origin https://github.com/DrKongVis/gitdemo.git #添加一个远程仓库，名字叫origin指向url
    - git push -u origin master                                      #将本地的归档区全部提交到远端的master分支

# 基本指令
- 提交用户信息
    - git config --global user.email "你的邮箱"：
    - git config --global user.name "用户名"

# 其他辅助指令
- git remote -v：查看远端的仓库
- git remote remove 仓库名：删掉远端仓库
- git status：查看本地仓库状态
- git log：查看一些提交信息
- git reflog：查看操作记录：用来还原
- git reset [opt] 版本号：代码回滚
    - [opt] = --mixed：回滚归档区、缓冲区
    - [opt] = --hard：回滚归档区、缓冲区、工作区
    - [opt] = --soft：回滚归档区
- git revert：删掉某个版本
- git fetch：获取远端的更新
- git pull [仓库名：默认是origin]：拉取远程仓库最新的版本并将远端同名分支合并到本地分支
- 在没有对master修改权限的情况下可以在github上点击pull request请求管理员合并分支

# 分支
- git branch -v：查看当前有哪些分支
- git checkout [选项] 分支名：切换到该分支
    - -b：创建分支
- git merge 分支名：将指定分支合并到当前分支
**解决冲突时，一般是将master分支marge到其他分支，解决了冲突后再修改master分支**