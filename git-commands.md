# Git命令

## 全局设置邮箱和用户名
- 设置邮箱
```
    $ git config --global user.email "your@email.com"
```
- 设置用户名
```
    $ git config --global user.name "your name"
```

## 初始化仓库
```
$ git init
```

## 添加文件
```
$ git add FILE_NAME
```

## 提交
```
$ git commit -m "message"
```

## 查看仓库状态
```
$ git status
```

## 比较文件状态
```
$ git diff FILE_NAME
```

## 查看历史记录
- 查看完整信息
```
    $ git log
```
- 查看简易信息
```
    $ git log --pretty==online
```

## 版本回退
- 回退至上一个版本
```
    $ git reset --hard HEAD^
```
- 回退至上两个版本
```
    $ git reset --hard HEAD^^
```
- 回退至上十个版本
```
    $ git reset --hard HEAD~10
```
- 回退至指定版本
```
    $ git reset --hard COMMIT_ID
```

## 查看HEAD指针变化历史记录
```
$ git reflog
```

## 丢弃指定文件在工作区的修改
```
$ git checkout -- FILE_NAME
```

## 删除文件
```
$ git rm FILE_NAME
```

## 添加一个远程仓库源
```
$ git remote add origin https://SERVER_NAME/USER_NAME/REPO_NAME.git
$ git remote add origin git@SERVER_NAME:USER_NAME/REPO_NAME.git
```

## 第一次推送
```
$ git push -u origin master
```

## 推送
```
$ git push origin master
```

## 克隆一个远程仓库到本地
```
$ git clone https://SERVER_NAME/USER_NAME/REPO_NAME.git
$ git clone git@SERVER_NAME:USER_NAME/REPO_NAME.git
```

## 创建新的分支
- 创建一个新的分支并指向该分支
```
    $ git checkout -b BRANCH_NAME
```
> 等价于下面两条命令
1. 创建一个新的分支
```
    $ git branch BRANCH_NAME
```
2. 指向该分支
```
    $ git checkout BRANCH_NAME
```

## 查看所有的分支
```
$ git branch
```

## 合并指定分支到当前分支
```
$ git merge BRANCH_NAME
```

## 删除指定分支
```
$ git branch -d BRANCH_NAME
```

## 查看分支合并图
```
$ git log --graph --pretty=oneline --abbrev-commit
```

## 禁用Fast Forward模式合并分支
```
$ git merge --no-ff -m "message" BRANCH_NAME
```

## 储藏当前工作区
```
$ git stash
```

## 查看储藏的工作区
```
$ git stash list
```

## 恢复储藏的工作区
1. 第一种方法
```
    $ git stash pop
```
2. 第二种方法
```
    $ git stash apply
    $ git stash drop
```
> 第一种方法恢复后会删除stash记录，第二种方法恢复后需要手动删除stash记录

## 丢弃一个未被合并的分支
```
$ git branch -D BRANCH_NAME
```

## 查看远程库的信息
1. 查看简易信息
```
$ git remote
```
2. 查看详细信息
```
$ git remote -v
```

## 推送分支
```
$ git push origin BRANCH_NAME
```
> 一般推送master分支

## 从远程抓取分支
```
$ git pull
```

## 在本地创建与远程分支对应的分支
```
$ git checkout -b BRANCH_NAME origin/BRANCH_NAME
```

## 建立本地分支与远程分支的关联
```
$ git branch --set-upstream BRANCH_NAME origin/BRANCH_NAME
```

## 变基
```
$ git rebase
```

## 查看标签
```
$ git tag
```

## 创建一个新的标签
```
$ git tag TAG_NAME
```
> TAG_NAME一般是版本号，例如：v1.0、v1.1

## 创建一个新的带有说明的标签
```
$ git tag -a v1.0 -m "Version 1.0 released" 1093d
```
> -a 指定标签名，-m 指定说明文字，1093d 为指定的COMMIT_ID

## 查看标签的信息
```
$ git show TAG_NAME
```

## 删除一个本地标签
```
$ git tag -d TAG_NAME
```

## 删除远程的一个标签
1. 第一步 删除本地的
```
    $ git tag -d TAG_NAME
```
2. 第二步 push到远程
```
    $ git push origin :refs/tags/TAG_NAME
```

## 推送一个本地的标签
```
$ git push origin TAG_NAME
```

## 推送所以的本地标签
```
$ git push origin --tags
```

## 关联多个远程
```
$ git remote add github git@github.com:USER_NAME/REPO_NAME.git

$ git remote add gitee git@gitee:USER_NAME/REPO_NAME.git
```

## 让Git显示颜色
```
$ git config --global color.ui true
```

## 编写.gitignore文件
> 忽略一些自动生成的文件或者是一些带有敏感信息的文件
### 强制添加被ignore的文件
```
$ git add -f FILE_NAME
```
### 查看文件是否被ignore
```
$ git check-ignore -v FILE_NAME
```

## 配置别名
```
$ git config --global alias.st status
```
> 将git status简化成git st