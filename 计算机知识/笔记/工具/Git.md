
### Git 是什么
Git 是一个免费、开源的分布式版本控制系统。它是由Linus Torvalds于2005年创建的。
<br/>

### 版本控制是什么
版本控制是一种系统或方法，用于跟踪和管理文件或项目在不同时间点的变化，并记录这些变化的历史。
<br/>

### Git 的主要功能

1. 版本控制：Git 能够跟踪文件的每个更改，记录文件的历史版本，并可轻松切换到不同的版本。

2. 分支管理：Git 具有强大的分支功能，允许用户创建、合并和删除分支。分支使得多人协作和并行开发变得更加灵活。

3. 协作与共享：Git 支持多人协作开发，可以将代码库克隆到不同的计算机上，并通过推送（Push）和拉取（Pull）操作与远程仓库进行交互。

4. 快速性能：Git 的设计追求高效性能。由于它是一个分布式版本控制系统，大部分操作都在本地执行，不需要依赖网络连接。

5. 回滚和恢复：Git 提供了撤销和回滚更改的功能，可以修复错误、恢复先前的状态或取消不必要的更改。

6. 可扩展性：Git 允许用户编写自定义脚本和钩子，以满足特定的工作流程需求。
<br>

### Git 用户设置
在第一次使用时， 我们需要初始化下git的配置：

- 告诉Git当前用户名称和邮件地址

```git
git --version // 检查版本
git config --global user.name "你的用户名"
git config --global user.email "你的邮件"
```

- 设置别名，以便可以使用简洁的命令

```git
git config --global alias.st status 
// git status 相当于 git st

git config --global alias.cm commit
```

- 设置系统所有用户别名
使用 sudo 管理权限可以给当前系统上所有git用户设置别名

```git
sudo git config --system alias.st status
```
<br>

### 工作流程
Git 的工作流程可以概括为以下几个基本步骤：

1. 初始化仓库：使用 `git init` 命令在项目目录中初始化一个新的 Git 仓库。这将创建一个 `.git` 隐藏目录，用于存储版本控制所需的元数据。

2. 添加文件：使用 `git add` 命令将文件添加到暂存区（Staging Area）,git会追踪暂存区所有文件。

3. 提交更改：使用 `git commit` 命令将暂存区中的文件变更提交到本地仓库。每次提交都会生成一个唯一的提交对象，包含了作者、提交时间、提交消息等信息。

4. 分支管理：使用各种分支操作命令（如 `git branch`、`git checkout`、`git merge`、`git rebase` 等）进行分支的创建、切换、合并、重命名、删除等操作。

5. 远程操作：使用 `git remote` 命令管理与远程仓库的交互。使用 `git clone` 命令克隆远程仓库到本地，使用 `git push` 命令将本地更改推送到远程仓库，使用 `git pull` 命令从远程仓库拉取最新的更改。

6. 历史查看和回滚：使用 `git log` 命令查看提交历史记录，使用 `git diff` 命令比较文件或提交之间的差异。通过 `git reset` 和 `git revert` 命令可以回退或撤销提交。
<br>

### Git 常用指令

配置：git config

```git
git config --global color.ui true // 设置全局配置,启用彩色输出现实
git config    //移除 --global 命令只对当前仓库生效

git config --list  // 查看git所有配置信息

git config --get user.name. // 查看当前配置用户名

git config --unset user.email  // 移除当前配置邮箱
```


日志：git log

```git
git log // 查看所有提交的历史记录。

git log -n 5  // 查看最近5条记录

git log --oneline -n 5  //  简短形式查看记录

git log --author=hayesyoung  // 查看指定作者记录

git log --since=2023-06-23 // 查看指定日期之后的记录

git log --until=2023-06-23  // 查看指定日期之前的记录

git log --grep="bug fix"  // 查看指定说明的记录，可以用关键词或者正则 

git log --grep="bug fix" -i  // grep 区分大小写，-i取消大小写 

git log --graph  // 以图形化方式显示提交历史
```

比较：git diff

```git
git diff  // 比较工作区中的文件与暂存区中的文件之间的差异。

git diff --staged


git diff a09f5c2 4adf037  // 比较两个指定的提交，哈希值、分支名或标签名都行
```



分支管理：git branch

```git
git checkout -b develop  // -b 是branch缩写， 表示创建并切换到新分支 "develop"
git branch -M main // 将当前分支的名称更改为 "main"

```



合并分支：git merge , git rebase

git merge 和 git rebase 的功能都是合并分支，区别在于，git merge 是将     ，git rebase 是将分支移植到master，


### Git flow
git flow 是一种基于git的分支管理工作流程，它提供了一套标准化的分支命名和管理规范.

1. 主分支（master）： 线上生产环境，部署稳定版本

2. 开发分支 （Develop）：日常开发

3. 功能分支（Feature）：开发新功能

4. 发布分支（Release）：用于发布新版本

5. 修复分支（Hotfix）：修复线上环境出现的问题



### Git tree



### 版本控制 



