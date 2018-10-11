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
```

## 第一次推送
```
$ git push -u origin master
```

## 推送
```
$ git push origin master
```
