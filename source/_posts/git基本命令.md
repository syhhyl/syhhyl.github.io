---
title: git基本命令
date: 2022-10-29 20:27:58
categories: git
---

# ==git==

## 初始化仓库



### 本地初始化

进入要进行git控制的项目目录（命令行），输入git init

```shell
git init
```



### 克隆远程仓库

进入你要保存远程仓库的目录，输入git clone <url>, 默认clone的仓库名与远程仓库名一致，如果要更改仓库名，url后加更改的仓库名

``` shell
# 默认仓库名
git clone url

#更改仓库名
git clone url new_name
```



## 添加并更新文件

每个文件无非两种状态：已跟踪或未跟踪

### tips

1.  如果是git init，本地默认是没有分支的，需要创建一个main分支

    ``` shell
    git branch -M main
    ```

2.  如果是git clone, 且远程仓库有默认分支，就不需要创建main分支。否则使用上面命令创建main分支



### 查看文件跟踪状态

``` shell
git status
```

### 添加文件

``` shell
# 添加filename这个文件
git add filename

# 添加当前目录下的所有文件
git add *
```

### 提交更新

``` shell
# info 为更新信息
git commit -m "info"
```





## 关联远程仓库

### 具体操作

``` shell
# remote_name 为远程仓库的别名
# token就是令牌，要自己生成
# user_name 就是你的github用户名
# repo_name就是远程仓库名
git remote add remote_name https://Token@github.com/user_name/repo_name.git
```





## 提交到远程仓库并合并

``` shell
git push repo_name <本地分支名>：<远程分支名>
```



## 拉取远程仓库合并到本地分支

``` shell
git pull repo_name <远程分支名>:<本地分支名>
```





---



## 分支管理

上面我们介绍了一个分支的情况，但是实际项目中我们会有多个分支要进行管理，所有下面是关于分支管理的相关命令。



| 命令                       | 作用             |
| -------------------------- | ---------------- |
| git branch / git branch -v | 查看所有分支     |
| git branch new_branchname  | 创建一个新分支   |
| git checkout branchname    | 切换分支         |
| git branch -d branchname   | 删除分支         |
| git merge branchname       | 合并分支到主分支 |





