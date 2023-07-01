
### Git 是什么
Git 是一个免费、开源的分布式版本控制系统。它是由Linus Torvalds于2005年创建的。
<br>

### 版本控制是什么
版本控制是一种系统或方法，用于跟踪和管理文件或项目在不同时间点的变化，并记录这些变化的历史。
<br>

### Git 的主要功能

1. 版本控制：Git 能够跟踪文件的每个更改，记录文件的历史版本，并可轻松切换到不同的版本。

2. 分支管理：Git 具有强大的分支功能，允许用户创建、合并和删除分支。分支使得多人协作和并行开发变得更加灵活。

3. 协作与共享：Git 支持多人协作开发，可以将代码库克隆到不同的计算机上，并通过推送（Push）和拉取（Pull）操作与远程仓库进行交互。

4. 回滚和恢复：Git 提供了撤销和回滚更改的功能，可以修复错误、恢复先前的状态或取消不必要的更改。

5. 可扩展性：Git 允许用户编写自定义脚本和钩子，以满足特定的工作流程需求。
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

2. 添加文件：将要进行版本控制的文件添加到 Git 仓库中。使用 `git add` 命令将文件添加到暂存区（Staging Area）。

3. 提交更改：使用 `git commit` 命令将暂存区中的文件变更提交到本地仓库。每次提交都会生成一个唯一的提交对象，包含了作者、提交时间、提交消息等信息。

4. 创建和切换分支：使用 `git branch` 命令可以创建新的分支，使用 `git checkout` 命令可以切换到不同的分支。分支允许并行开发和独立的工作流。

5. 合并分支：使用 `git merge` 命令将一个分支的更改合并到当前分支。合并会将两个分支的修改整合到一起，并生成一个新的提交。

6. 远程操作：使用 `git remote` 命令管理与远程仓库的交互。使用 `git clone` 命令克隆远程仓库到本地，使用 `git push` 命令将本地更改推送到远程仓库，使用 `git pull` 命令从远程仓库拉取最新的更改。

7. 分支管理：使用各种分支操作命令（如 `git branch`、`git checkout`、`git merge`、`git rebase` 等）进行分支的创建、切换、合并、重命名、删除等操作。

8. 历史查看和回滚：使用 `git log` 命令查看提交历史记录，使用 `git diff` 命令比较文件或提交之间的差异。通过 `git reset` 和 `git revert` 命令可以回退或撤销提交。
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

git branch -vv   // 查看本地分支及其跟踪信息
```




合并分支：git merge , git rebase

git merge 和 git rebase 的功能都是合并分支，区别在于，git merge 是将     ，git rebase 是将分支移植到master，






### 版本控制
版本控制也可以叫

### 分支管理


### Git tree



### Git flow
git flow 是一种基于git的分支管理工作流程，它提供了一套标准化的分支命名和管理规范.

1. 主分支（master）： 线上生产环境，部署稳定版本

2. 开发分支 （Develop）：日常开发

3. 功能分支（Feature）：开发新功能

4. 发布分支（Release）：用于发布新版本

5. 修复分支（Hotfix）：修复线上环境出现的问题



















![[gitbranchvv20230630191328.png]]

* * 表示当前分支
* main 分支跟踪了 `origin/master` 的远程分支
* 

Git 是一个分布式版本控制系统，它的原理主要包括以下几个关键概念和机制：

1. 代码仓库（Repository）：Git 将项目的完整历史记录存储在一个名为代码仓库的地方。仓库包含了项目的所有文件、目录以及它们的完整历史快照。

2. 提交（Commit）：在 Git 中，提交是指将当前工作目录的状态保存到代码仓库中的一个快照。提交包括作者、提交时间、提交消息以及指向前一个提交的指针。

3. 分支（Branch）：分支是指代码仓库中的一个可独立开发和修改的副本。分支可以基于其他分支创建，从而形成一个分支树。每个分支都有自己的提交历史。

4. 标签（Tag）：标签是指向特定提交的静态引用。与分支不同，标签通常用于标记项目的里程碑或发布版本。

5. 远程仓库（Remote Repository）：远程仓库是指位于网络上的另一个 Git 仓库。它可以用来共享代码和协同开发。常见的远程仓库服务有 GitHub、GitLab 和 Bitbucket。

6. 克隆（Clone）：克隆是指从远程仓库中复制整个项目的操作。克隆将创建一个与原始仓库完全相同的副本，包括历史记录和分支。

7. 拉取（Pull）：拉取是指从远程仓库获取最新更改并合并到本地仓库的操作。它包括两个步骤：获取（Fetch）远程仓库中的更新和合并（Merge）更新到当前分支。

8. 推送（Push）：推送是指将本地仓库的更改上传到远程仓库的操作。它将本地分支的提交推送到远程分支，并使远程仓库与本地仓库保持同步。


### Git 分支管理
Git 的分支管理是其强大功能之一，它允许开发者创建、切换、合并、删除和管理分支，以支持并行开发和团队协作。下面是 Git 分支管理的一般流程：

1. 创建分支：使用 `git branch <branch-name>` 命令创建一个新的分支。例如，`git branch feature` 将创建一个名为 "feature" 的分支。

2. 切换分支：使用 `git checkout <branch-name>` 命令切换到所需的分支。例如，`git checkout feature` 将切换到名为 "feature" 的分支。

3. 查看分支：使用 `git branch` 命令查看所有存在的分支，并在当前分支前添加一个星号。例如，`git branch` 将列出所有分支及当前所在的分支。

4. 提交更改：在所选分支上进行开发和修改，并使用 `git add` 和 `git commit` 命令将更改提交到该分支的本地仓库。

5. 合并分支：当一个分支的开发完成后，可以将其合并到主分支或其他目标分支上。使用 `git merge <branch-name>` 命令将指定分支的更改合并到当前分支。

6. 解决冲突：在合并分支时，如果有冲突（两个分支对同一文件的同一部分进行了修改），需要手动解决冲突。Git 会标记冲突的文件，你需要打开这些文件并手动编辑，解决冲突后再次提交。

7. 删除分支：使用 `git branch -d <branch-name>` 命令删除已经合并的分支。例如，`git branch -d feature` 将删除名为 "feature" 的分支。如果分支未合并，可以使用 `git branch -D <branch-name>` 命令强制删除分支。

8. 远程分支管理：使用 `git push` 命令将本地分支推送到远程仓库，使用 `git pull` 命令从远程仓库拉取最新的分支信息。