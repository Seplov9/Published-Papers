# Git structure

              +-------------+         +-------------+        +-------------+        +---------------+
              | Working Dir |  --->   |   Staging   |  --->  | Local Repo  | --->   |  Romote Repo  |
                   工作区      --->        暂存区       --->     本地仓库      --->        远程仓库     
              +-------------+         +-------------+        +-------------+        +---------------+


# Git command cheetsheet

|                              | From    | To                   | Info                       |
| ---------------------------- | ------- | -------------------- | -------------------------- |
| git add ./<file>             | working | staging              |                            |
| git commit                   | staging | local                |                            |
| git commit -a                | working | local                | once added files           |
| git commit --amend           |         |                      | old commint infonew commit |
| git push origin <branch>     | local   | remote               |                            |
|                              |         |                      |                            |
| git restore <file>           | working | working(last commit) | withdraw modification      |
| git checkout -- <file> [old] |         |                      |                            |
|                              |         |                      |                            |
| git restore --stage <file>   | staging | working              | withdraw add               |
| git reset HEAD <file> [old]  |         |                      |                            |
|                              |         |                      |                            |
| git reset --soft HEAD~1(2)   | local   | staging              | withdraw commit            |
| git reset --soft HEAD^(^^)   |         |                      |                            |
| git reset --mixed HEAD~1     | local   | working              |                            |
| git reset HEAD~1             |         |                      |                            |
| git reset --hard HEAD~1      | local   | none                 |                            |
|                              |         |                      |                            |
| git revert HEAD              | remote  | none                 | safe withdraw push         |


# Daily devlopment
// 如何根据主分支更新开发分支

$ git checkout main/develop // checkout到主分支

$ git pull                  // 更新主分支内容，更新来自其他开发者的commits

$ git checkout <branch>     // checkout到自己的开发分支

$ git rebase main/develop   // 通过rebase，与主分支进度保持一致

// 提交开发分支以及PR

$ git push -u origin <branch>

// github上提交PR

$ git commit -C HEAD        // 根据reviewer反馈进行修改，-C HEAD 复用前一个commit msg

# Final merge，最终代码合入主分支
// 在开发分支加入主分支的更新

$ git checkout main/develop

$ git pull

$ git checkout <branch>

$ git rebase main/develop

// especially when main/develop branch is updated

$ git commit --amend

$ git push -u -f origin <branch>

Status check

Please use "git status" frequently, as well as other git commands, to check the status.

# Git setting

$ git config --global user.name "<user_name>"

$ git config --global user.email "<user_name>@is.ic"

$ git config --global commit.template ~/.gitmessage.txt

$ git config --global core.editor "nano"  # in Powershell, ignore it in zsh

$ git config --global core.editor "code --wait"  # not recommended

// .gitmessage

// Powershell

$ cd ~

$ vim .gitmessage.txt

  type [SCOPE]: short-summary
  
  Problem:
  
  description of the problem being solved
  
  Solution:
  
  description of the solution implemented
  
  Test:
  
  description of how the change was tested
  
  JIRA: ISSUE-Number

// Shell

$ cat << 'EOF' | tee ~/.gitmessage.txt

type [SCOPE]: <hort-summary

Problem:

description of the problem being solved

Solution:

description of the solution implemented

Test:

description of how the change was tested

JIRA: ISSUE-Number

EOF

$ ssh-keygen -t rsa -b 2048 -C "<user_name>@is.ic"

$ cat ~/.ssh/id_rsa.pub

# PR

// Step 1: checkout right branch

// Step 2: pytest

// Step 3: activate pre-commit

$ pre-commit install

// step 4: PR

$ git add ./file name

$ git commit

// into vim, nano or vscode

// first time

$ git push -u origin <branch>

//  not first time

$ git commit -C HEAD

$ git push

//  On github.com/repository website

//  Click "Compare & pull request"

//  Add title

  type[SCOPE]: short-summary
  
// Add discription

  Problem:
  
  - description of the problem being solved
  
  Solution:
  
  - description of the solution implemented
  
  Test:
  
  - description of how the change was tested
  
  JIRA: ISSUE-Number
  
  // after "JIRA: ISSUE-<Number>", type '#' to choose the right <Number> link

// Click "Create pull request"

// Add reviewers

// Review and revise

// For gemini-code-assist advisement

// Reply "take it" if use it

// Reply "reject it" and explaination if omit it

// Click "Squash and merge"

// In this way, keep one complete commit message and delete the rest.

// Notes

// 1. After "pre-commit install", it will automatically check all files when submit "git commit". If code have been revised, please re-go through the PR process.

// 2. Please not use "git push -f" in case this operation will cover all commit messages, resulting in the loss of commit records.

# UV

// install uv

// macOS/Linux

$ curl -LsSf https://astral.sh/uv/install.sh | sh

// Windows

$ powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"

// macOS

$ brew install uv

// Or via pip

$ pip install uv

// setup development environment

// Create virtual environment and install dependencies

$ Set-ExecutionPolicy-ExecutionPolicy Bypass-Scope Process/CurrentUser # only for the first time

$ uv sync

// Activate the virtual environment

// Linux/macOS

$ source .venv/bin/activate

// Windows

$ .venv\Scripts\activate

// UV command cheetsheet

// create virtual environment

$ uv venv --python <env_name>

// pip

$ uv pip install <package_name>
