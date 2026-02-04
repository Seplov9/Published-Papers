Git Getting Started （Git基本用法介绍，可跳过）
Git structure
              +-------------+         +-------------+        +-------------+        +---------------+
              | Working Dir | --->   |    Staging    | --->  | Local Repo  | ---> | Romote Repo |
                     工作区       --->         暂存区       --->       本地仓库     --->        远程仓库     
              +-------------+         +-------------+        +-------------+        +---------------+

Git command cheetsheet

From
To
Info
git add ./<file>
working
staging

git commit
staging
local

git commit -a
working
local
once added files
git commit --amend


old commint info
new commit
git push origin <branch>
local
remote





git restore <file>
working
working(last commit)
withdraw modification
git checkout -- <file> [old]







git restore --stage <file>
staging
working
withdraw add
git reset HEAD <file> [old]







git reset --soft HEAD~1(2)
local
staging
withdraw commit
git reset --soft HEAD^(^^)



git reset --mixed HEAD~1
local
working

git reset HEAD~1



git reset --hard HEAD~1
local
none





git revert HEAD
remote
none
safe withdraw push

Daily devlopment
# 如何根据主分支更新开发分支
$ git checkout main/develop # checkout到主分支
$ git pull                  # 更新主分支内容，更新来自其他开发者的commits
$ git checkout <branch>     # checkout到自己的开发分支
$ git rebase main/develop   # 通过rebase，与主分支进度保持一致

# 提交开发分支以及PR
$ git push -u origin <branch>
# github上提交PR
$ git commit -C HEAD        # 根据reviewer反馈进行修改，-C HEAD 复用前一个commit msg

Final merge，最终代码合入主分支
# 在开发分支加入主分支的更新
$ git checkout main/develop
$ git pull
$ git checkout <branch>
$ git rebase main/develop

# especially when main/develop branch is updated
$ git commit --amend
$ git push -u -f origin <branch>

Status check
Please use "git status" frequently, as well as other git commands, to check the status.
