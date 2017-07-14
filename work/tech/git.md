# 《Pro Git》笔记

链接：[git-scm](https://git-scm.com/book/zh/v2/)

# 简介
1. Git是以全量快照为版本的，并不是像svn以差异文件为版本
2. Git是分布式版本控制，每个Git clone中都有所有所有历史

# 模型

本地文件->缓存->本地数据库->远程数据库

- 本地文件需要添加到缓存中，才能提交
- 每次添加缓存都会在缓存中产生一个快照
- 修改本地文件对缓存中的快照不产生影响
- 没有放到缓存中的文件不会被提交

![存储区](res/git_storage.png)

![文件状态](res/git_file_status.png)

# 配置
## 配置文件
配置文件存在于系统和个人目录中：
- /etc/gitconfig
- ~/.gitconfig

文件结构如下：
```shell
[user]
    name = jiaoyang623
    email = jiaoyang623@qq.com
[core]
    autocrlf = input
    editor = vim
[push]
    default = simple
[credential]
    helper = store

```
其中保存了用户名、默认编辑器等信息
## 配置操作
如命令所示调用git config进行操作。使用--global则会写到配置文件中；如果不使用--global，则只会对当前提交产生影响。
```shell
git config --global user.name 'jiaoyang623'
git config --global core.editor vim
```
## 查看配置
```shell
# 查看当前能找到的配置
git config --list

# 查看某个配置
git config user.name
```

# 操作

## 初始化
```shell
# 初始化本地文件夹
git init

# 克隆现有仓库
git clone https://github.com/libgit2/libgit2
```

## 更新

```shell
# 查看状态
git status

# 状态简览
git status -s

# 跟踪文件/暂存文件
git add FILENAME

# 对比
git diff

# 
git diff --staged
```


# 实践
