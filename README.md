\1. 什么是Git？

GIT，全称是分布式版本控制系统，git通常在编程中会用到，并且git支持分布式部署，可以有效、高速的处理从很小到非常大的项目版本管理。分布式相比于集中式的最大区别在于开发者可以提交到本地，每个开发者通过克隆（git clone），在本地机器上拷贝一个完整的Git仓库。

\2. 简述一下git的工作流程

- 克隆 Git 资源作为工作目录。
- 在克隆的资源上添加或修改文件。
- 如果其他人修改了，你可以更新资源。
- 在提交前查看修改。
- 提交修改。
- 在修改完成后，如果发现错误，可以撤回提交并再次修改并提交。

\3. 写出10个git常用指令，并解释其含义

- git init - 初始化仓库。
- git add . - 添加文件到暂存区。
- git commit - 将暂存区内容添加到仓库中。

### 创建仓库命令

下表列出了 git 创建仓库的命令：

| 命令        | 说明                                   |
| :---------- | :------------------------------------- |
| `git init`  | 初始化仓库                             |
| `git clone` | 拷贝一份远程仓库，也就是下载一个项目。 |

## 提交与修改

Git 的工作就是创建和保存你的项目的快照及与之后的快照进行对比。

下表列出了有关创建与提交你的项目的快照的命令：

| 命令         | 说明                                     |
| :----------- | :--------------------------------------- |
| `git add`    | 添加文件到暂存区                         |
| `git status` | 查看仓库当前的状态，显示有变更的文件。   |
| `git diff`   | 比较文件的不同，即暂存区和工作区的差异。 |
| `git commit` | 提交暂存区到本地仓库。                   |
| `git reset`  | 回退版本。                               |
| `git rm`     | 删除工作区文件。                         |
| `git mv`     | 移动或重命名工作区文件。                 |

### 提交日志

| 命令         | 说明                                 |
| :----------- | :----------------------------------- |
| `git log`    | 查看历史提交记录                     |
| `git blame ` | 以列表形式查看指定文件的历史修改记录 |

### 远程操作

| 命令         | 说明               |
| :----------- | :----------------- |
| `git remote` | 远程仓库操作       |
| `git fetch`  | 从远程获取代码库   |
| `git pull`   | 下载远程代码并合并 |
| `git push`   | 上传远程代码并合并 |

\4. 简述一下git 分支的作用

git分支就是在版本控制过程中，使用多条线同时推进多个任务

一个项目里，主分支master分为几部分分支feature，处理不同的部分，如，一个游戏项目，可以分出搞图像的、搞运算的、操作的等分支。在公司里，每个团队处理属于自己的分支，不同部门分支互不干扰，也不影响主分支，假如某个分支出现严重错误，只需要删除这个分支重新来过，其他分支没影响。当一个分支开发完成，就把他合并到主干中，全部分支开发完后，最终形成整个项目。然而，主干master也可能出现bug，这个时候就有一个host_fix分支（临时分支，用来修复bug，修复完及时合并为主干）

\5. git rebase 和 git merge的区别

接[Git分支创建与合并](http://www.cnblogs.com/shuimuzhushui/p/8999445.html)，在分支合并时，有两种方式：git merge 和git rebase。

git merge：将两个分支，合并提交为一个新提交，并且新提交有2个parent。

git rebase：会取消分支中的每个提交，并把他们临时存放，然后把当前分支更新到最新的origin分支，最后再吧所有提交应用到分支上。