---
title: Git基础教程
categories:
- 版本控制
tags:
- Git
abbrlink: 29126
---

# Git开发命令

```bash
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M master 
git remote add origin git@*.git
git push -u origin master
```

```bash
git init                     // 新建 git 代码库
// 创建开发分支
git co(checkout) -b develop  
git push  // 推送分支到远程仓库

// 个人提交代码到远程仓库
git add .
git st(status)
git diff // 查看文件 diff文件的修改
git ci(commit)  -m "内容" 本次修改
git push 

git commit --amend # → 将暂存区和当前commit合并创建一个新commit去替换当前commit

git stash # → 把当前的工作隐藏起来 等以后恢复现场后继续工作
git stash pop # → 恢复工作现场（恢复隐藏的文件，同时删除stash列表中对应的内容）

// 远程分支管理
git fetch --all  // 拉取所有远端的最新代码 
git merge origin/develop // 多人协作 合并同事开发的分支
get merge origin/master
git push 
git merge --no-ff origin/develop   # → 同事review code之后管理员合并origin/develop到远端主干origin/master


git add <filename>                     // 添加指定文件到暂存区
git rm                       // 删除工作区文件，并且将这次删除放入暂存区
git commit -m [message]      // 提交暂存区到仓库区

git commit -am(-a -m) === git add . 和 git commit -m ""
git commit ./xx   # 等同于git add ./xx + git commit

git branch                   // 列出所有分支
git branch dmeo // 创建
git branch  -d demo // 删除
git checkout -b [branch]     // 新建一个分支，并切换到该分支 git switch -c [branch]
git commit -m "" -a  // 相当于 git add . 加 git commit -m ""
git status                   // 显示有变更的文件
// 推送分支
git push origin demo-2
git config --global credential.helper store // 记住账号密码
// 配置公钥 -t 类型 rsa 非对称加密 -C 地址
goit merge 
ssh-keygen -t rsa -C "youremal@example.com"
// 公钥 私钥
// 上线 打标签 标签列表
git tag --list //
git tag v1.0.0
git push origin v1.0,0
// 只是删除本地
git tag -d v1.0.0

git push origin :t1.0.1 // 删除云端
git push origin master --force
// 回滚 到本地 不删除云端回滚记录
git revert <commit> // 版本号
// 回滚 删除云端回滚记录
git reset --hard <commit>
git push origin demo --force // demo 分支
```

# Git开发问题

>  [git branch ~(END) on terminal?](https://stackoverflow.com/questions/51015733/git-branch-end-on-terminal)
>
> You can replace the pager with `less` so it doesn't "scroll" outputs less than the height of the terminal.
>
> ```
> git config --global --replace-all core.pager "less -F -X"
> ```
>
> I found it from this q. Took a while to find compared to OPs questions, so I figured I'd drop it here in case anyone else has the same issue.
>
> git merge bugos
> hint: Waiting for your editor to close the file... Error detected while processing /Users/administrator/.vimrc:
> line    2:
> E492: Not an editor command: setcursorline
> Press ENTER or type command to continu

# Git基础教程

可以从Git的操作是一种高级备份的角度来理解Git相关命令

```
git help 
```

## 回滚操作

## 相关命令

`怎么进入具体的目录`

```cmd
cd D:\GitRepository\GithubProject // 目录位置
d： 目录的盘符  或 D:	
ls -a // 查看隐藏目录
Mac 
cd ~ // ~ == /Users/administrator
cd 回退到上一层
```

> linux ls命令:
>
> -F 给不同的文git件添加不同表示,添加帽子
>
> d/   l*  =s 
>
> -a: 显示隐藏文件  以.开头的文件
>
> -p: 只给目录添加/
>
> -t: 按照修改时间排序 time
>
> --time-style=long-iso: ls -l --time-style=long-iso  显示友好长格式时间
>
> -r: 倒着排序 reverse
>
> -S: 按照文件大小排序
>
> -h: 以人类理解的范围显示
>
> -i: 索引节点(inode==书的目录) print the index number of each file(内核根据此区别文件是否同一文件)

## 基本概念

> 概念
>
> - CVS及SVN都是集中式的版本控制系统。
> 	- 版本管理就是管理更新的历史记录
> - Git是分布式版本控制系统，极其强大的分支管理。
>
> 功能
>
> - 记录一款软件添加或更改源代码的工程
> - 回滚到特定阶段，恢复误删除的文件
> - 合并多人协作的文件等
> - 多人协同，文件传输
>
> 四大库
>
> - 四大库的关系相当于 本地仓库（commit    暂存区 历史副本 《= add 工作区 当前版本 ） 《==》 远程仓库
> 	- commit 添加标签
> 	- add 添加历史副本
> - 工作区（本地文件夹）：本地电脑存放项目文件的地方，比如learnGitProject文件夹；
> - 暂存区：（Index/Stage）：在使用git管理项目文件的时候，其本地的项目文件会多出一个.git的文件夹，将这个.git文件夹称之为版本库。其中.git文件夹中包含了两个部分，一个是暂存区（Index或者Stage）,顾名思义就是暂时存放文件的地方，通常使用add命令将工作区的文件添加到暂存区里；
> - 本地仓库：.git文件夹里还包括git自动创建的master分支，并且将HEAD指针指向master分支。使用commit命令可以将暂存区中的文件添加到本地仓库中；
> - 远程仓库（Github、Gitee、GitLab）：不是在本地仓库中，项目代码在远程git服务器上，比如项目放在github上，就是一个远程仓库，通常使用clone命令将远程仓库拷贝到本地仓库中，开发后推送到远程仓库中即可。

## 基本配置

查看配置

```bash
git config -list
git config -l

#查看系统config
git config --system --list　
#查看当前用户（global）配置
git config --global  --list
#查看当前仓库配置信息
git config --local  --list
```

设置name和email

```bash
// username useremail
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```

初始化仓库

```bash
git init	
```

仓库状态

```bash
git status // git st
```

查看修改内容

工作区与暂存区的差异

```bash
git diff <file name> //查看 difference 指定文件在工作区和暂存区上差异比较
// 比较工作区中当前文件和暂存区之间的差异，也就是修改之后还没有暂存的内容： 
```

从版本库中删除该文件

```bash
rm -rf test.txt // 工作区删除git rm test.txt // 删除工作区文件，并且也从暂存区删除对应文件的记录 ?git rm --cached test.txt // 从暂存区中删除文件，但是工作区依然还有该文件 （暂存区删除文件）
```

#### Git显示颜色

```bash
git config --global color.ui truegit config --global core.editor vi
```

```
git mv [file-original] [file-renamed]; 重命名文件，并将已改名文件提交到暂存区：
```

```
git commit -m ""  vs git tag 
```

```
// 将所有已经使用git管理过的文件暂存后一并提交，跳过add到暂存区的过程：git commit -a -m "commit_info";
```

```
git log 参数-p展开每次提交的内容差异，用-2显示最近的两次更新，如git log -p -2

 git log xx  # → 查看xx文件的commit记录

$ git log -p xx   # → 查看xx文件每次提交的diff
$ git log --pretty=oneline xx  # → 查看xx文件提交的历史记录（只显示哈希值和提交说明）

$ git log --pretty=raw  # → 查看commit之间的父子关系（root commit是没有父提交的）
$ git log --graph  # → 查看当前分支commit生成的树状图
```

## 版本管理

![Git经典流程图](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a1d538d63559402fbcfd82d68b08061c~tplv-k3u1fbpfcp-watermark.awebp)

### 本地仓库|暂存区|工作区

- 版本库（Respository） 
	工作区有一个隐藏目录`.git`，这个不算工作区，而是Git的版本库。
	Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的**暂存区**，还有Git为我们自动创建的第一个分支`master`，以及指向`master`的一个指针叫`HEAD`。
- 工作区：工作区（Working Directory） 就是你在电脑里能看到的目录
	前面讲了我们把文件往Git版本库里添加的时候，是分两步执行的：
	第一步是用`git add`把文件添加进去，实际上就是把文件修改添加到暂存区；
	第二步是用`git commit`提交更改，实际上就是把暂存区的所有内容提交到当前分支。

```
git add readme.txt
git commit -m "wrote a readme file"
```

`git add`命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，
执行`git commit`就可以一次性把暂存区的所有修改提交到分支。

### 把文件修改添加到暂存区 vs 从暂存区恢复文件到工作区

本地仓库（打了标签的历史备份） 《=》 暂存区  (最近的一次历史备份)  《==》 工作区  

- 工作区  《==》 暂存区  add(备份)、restore(还原) 可以理解为当前的手机资料丢失了要重本地备份的暂存区中还原
- 本地仓库 《==》工作区 commit 给每一次标签都添加上一个标签(时间段、备份信息)

git state 查看暂存区的状态 

git log 查看本地仓库的状态 

```bash
// 文件修改添加到暂存区git add readme.txtgit add . // 工作区到暂存区git commit -m "wrote a readme file" //First modification 第一次修改 // 暂存区到本地仓库
// 暂存区恢复文件到工作区
git restore <file-name>
// 还原多个文件时怎么处理？
git restore .

// git state  vs  git log
```

```bash
git diff 文件名 // 暂存区与工作区的区别
git diff HEAD --readme.txt	// 查看修改
```

从本地仓库还原到工作区 

```bash
git checkout -- <file>
```

添加到了暂存区时，想丢弃修改
场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令`git reset HEAD `，就回到了场景1，第二步按场景1操作。

删除暂存区备份 

```bash
git reset HEAD <file> 
//回退版本，也可以把暂存区的修改回退到工作区。当我们用HEAD时，表示最新的版本。
git checkout -- file
```

###### 删除文件

命令`git rm`用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失**最近一次提交后你修改的内容**。

1. 工作区中删除文件

```bash
rm test.txt
```

2. 要从版本库中删除该文件，那就用命令`git rm`删掉，并且`git commit`：

```
git rm test.txt
git commit -m "remove test.txt"
```

3. 删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：

```bash
git checkout -- test.txt
```

`git checkout`其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

### 版本回退

回退历史版本

`git log`可以查看提交历史，以便确定要**回退到哪个版本**。

```
git loggit log --pretty=oneline  //输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数 漂亮 oneline 线上一线女装
```

`git reflog`查看命令历史，以便确定要**回到未来的哪个版本**。

```bash
git refloggit reflog --pretty=oneline 
```

修改到版本库

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考[版本回退](https://www.liaoxuefeng.com/wiki/896043488029600/897013573512192)一节，不过前提是没有推送到远程库。

```bash
git reset --hard HEAD^  //下一个版本git reset --hard 版本号 //版本号不用写全// 很努力的重置reset 重置；清零hard  努力的；硬的；困难的
```

```bash
git reset --hard 版本号 //git reset --hard HEAD^  //下一个版本
git log
git reflog
```

Git显示从最近到最远的提交日志`HEAD`指向的版本就是当前版本

```bash
git reset --hard HEAD^  //下一个版本
git reset --hard 版本号 //版本号不用写全
```

## 远程库管理

#### 配置SSH添加公钥（id_rsa.pub）到远程账号账号(id_rsa//id_rsa.pub) 登陆文件

- 公钥与私钥

```bash
// 查看有没有公钥cd C:\Users\Administrator\.ssh\id_rsa.pubC:cd ~/.sshls// 生成公钥ssh-keygen -t rsa -C "youremail@example.com" 1. ssh-keygen -t rsa -C "15816073129@163.com" // ssh key gen  -t RSA算法 Keygen为Key Generator的简写形式就是一般所说的注册机2. 输入密码验证是否成功，在git bash下输入ssh -T git@github.comssh -T git@gitee.com接下来我们要做的就是把本地仓库传到github上去，在此之前还需要设置username和email，因为github每次commit都会记录他们git config --global user.name"your name"git config --global user.email"your_email@youremail.com"// 添加公钥到远程仓库
```

#### 关联GitHub的远程库

```bash
git remote add gitee git@gitee.com:code-dream/CS-Xmind-Note.git
```

#### 删除已有的GitHub远程库：

```bash
git remote rm origin //git给远程库起的默认名称是`origin`
```

#### 查看远程库信息：

```bash
git remote -v
```

#### 同时关联Github和Gitee

关联GitHub的远程库：

```bash
git remote add github git@github.com:michaelliao/learngit.git
```

关联Gitee的远程库：

```bash
git remote add gitee git@gitee.com:liaoxuefeng/learngit.git
```

#### 查看远程库信息，可以看到两个远程库：

```bash
git remote -vgitee	git@gitee.com:liaoxuefeng/learngit.git (fetch)gitee	git@gitee.com:liaoxuefeng/learngit.git (push)github	git@github.com:michaelliao/learngit.git (fetch)github	git@github.com:michaelliao/learngit.git (push)
```

如果要推送（上传）到GitHub，使用命令：

```bash
git
```

如果要推送（上传）到Gitee，使用命令：

```bash
git push gitee master
```

#### 克隆

```bash
git clone 仓库地址
```

fetch  

- 将远程仓库内容更新到本地

```bash
git fetch <远程主机名>
git fetch <远程主机名> <分支名> // 取回特定分支
git fetch orgin  <branch-name> <local-name>
```

##### 远程程库：Github、Gittee、GitLab。提供Git仓库托管服务的。

GitHub作为免费的远程仓库

- 在GitHub上，可以任意Fork开源仓库；
- 自己**拥有Fork后的仓库的读写权限**；
- 可以推送pull request给官方仓库来贡献代码。
	Gittee(码云)
- 国内的Git托管服务——[Gitee](https://gitee.com/?utm_source=blog_lxf)（[gitee.com](https://gitee.com/?utm_source=blog_lxf)）
	GitLab

##### 添加远程库

##### 从远程库克隆

##### 使用GitHub

GitHub是免费的远程仓库、一个开源协作社区。

- 在GitHub上，可以任意Fork开源仓库；
	Fork就是把别人的仓库项目**克隆**在自已的仓库项目
- 自己**拥有Fork后的仓库的读写权限**；
- 可以推送pull request给官方仓库来贡献代码。

```bash
git clone 仓库地址
```

如果从别人的仓库地址克隆，因为没有权限，你将**不能推送修改**。

##### 使用Gitee（码云）

国内的Git托管服务——[Gitee](https://gitee.com/?utm_source=blog_lxf)

###### 上传自己的SSH公钥

选择右上角用户头像 -> 菜单“修改资料”，然后选择“SSH公钥”，填写一个便于识别的标题，然后把用户主目录下的`.ssh/id_rsa.pub`(C:\Users\Administrator\.ssh)文件的内容粘贴进去：

###### 配置SSH添加公钥（id_rsa.pub）到远程账号账号(id_rsa//id_rsa.pub)

```bash
// 查看有没有公钥
C:\Users\Administrator\.ssh\id_rsa.pub
// 没有生成公钥
ssh-keygen -t rsa -C "youremail@example.com" 
// 添加公钥到远程仓库
```

###### 关联到Gitee的远程库

```bash
git remote add origin 具体项目的仓库地址  //remote 远程  + origin 起源
```

###### 删除已有的GitHub远程库：

```
git remote rm origin //git给远程库起的默认名称是`origin`
```

###### 查看远程库信息：

```
git remote -v
```

如果在使用命令`git remote add`时报错：

```bash
git remote add origin git@gitee.com:liaoxuefeng/learngit.git
fatal: remote origin already exists.
```

这说明本地库已经关联了一个名叫`origin`的远程库，此时，可以先用删除远程库，再关联：

###### 一个本地库既关联GitHub，又关联Gitee

git本身是分布式版本控制系统，可以同步到另外一个远程库，当然也可以同步到另外两个远程库。
**使用多个远程库时，我们要注意，git给远程库起的默认名称是`origin`，如果有多个远程库，我们需要用不同的名称来标识不同的远程库。**
关联GitHub的远程库：

```bash
git remote add github git@github.com:michaelliao/learngit.git
```

关联Gitee的远程库：

```bash
git remote add gitee git@gitee.com:liaoxuefeng/learngit.git
```

查看远程库信息，可以看到两个远程库：

```bash
git remote -v
gitee	git@gitee.com:liaoxuefeng/learngit.git (fetch)
gitee	git@gitee.com:liaoxuefeng/learngit.git (push)
github	git@github.com:michaelliao/learngit.git (fetch)
github	git@github.com:michaelliao/learngit.git (push)
```

如果要推送（上传）到GitHub，使用命令：

```bash
git push github master
```

如果要推送（上传）到Gitee，使用命令：

```bash
git push gitee master
```

###### 自定义Git

在[安装Git](https://www.liaoxuefeng.com/wiki/896043488029600/896067074338496)一节中，我们已经配置了`user.name`和`user.email`，实际上，Git还有很多可配置项。
比如，让**Git显示颜色**，会让命令输出看起来更醒目：

```bash
git config --global color.ui true
```

###### 忽略特殊文件

- `.gitignore`文件，把要忽略的文件名填进去，Git就会自动忽略这些文件。
- `.gitignore`文件本身要放到版本库里，并且可以对`.gitignore`做版本管理！

###### 搭建Git服务器

- 自己搭建一台Git服务器作为私有仓库使用。
- 推荐用Ubuntu或Debian，这样，通过几条简单的`apt`命令就可以完成安装。
- 搭建Git服务器非常简单，通常10分钟即可完成；
- 要方便**管理公钥**，用[Gitosis](https://github.com/sitaramc/gitolite)；
- 要像SVN那样变态地**控制权限**，用[Gitolite](https://github.com/sitaramc/gitolite)。
	**第一步，安装`git`**：

```
$ sudo apt-get install git
```

**第二步，创建一个`git`用户，用来运行`git`服务：**

```
$ sudo adduser git
```

**第三步，创建证书登录：**
**收集所有需要登录的用户的公钥**，就是他们自己的`id_rsa.pub`文件，把所有公钥导入到`/home/git/.ssh/authorized_keys`文件里，一行一个。
**第四步，初始化Git仓库：**
先选定一个目录作为Git仓库，假定是`/srv/sample.git`，在`/srv`目录下输入命令：

```
$ sudo git init --bare sample.git
```

Git就会创建一个裸仓库，裸仓库没有工作区，因为服务器上的Git仓库纯粹是为了共享，所以不让用户直接登录到服务器上去改工作区，并且服务器上的Git仓库通常都以`.git`结尾。然后，把owner改为`git`：

```
$ sudo chown -R git:git sample.git
```

**第五步，禁用shell登录：**
出于安全考虑，第二步创建的git用户不允许登录shell，这可以通过编辑`/etc/passwd`文件完成。找到类似下面的一行：

```
git:x:1001:1001:,,,:/home/git:/bin/bash
git:x:1001:1001:,,,:/home/git:/usr/bin/git-shell
```

这样，`git`用户可以正常通过ssh使用git，但无法登录shell，因为我们为`git`用户指定的`git-shell`每次一登录就自动退出。
**第六步，克隆远程仓库：**
现在，可以通过`git clone`命令克隆远程仓库了，在各自的电脑上运行：

```
$ git clone git@server:/srv/sample.git
Cloning into 'sample'...
warning: You appear to have cloned an empty repository.
```

## 分支管理

**在Git里，这个分支叫主分支，即`master`分支。`HEAD`严格来说不是指向提交，而是指向`master`，`master`才是指向提交的，所以，`HEAD`指向的就是当前分支。**
Git的分支是与众不同的，无论创建、切换和删除分支，Git在1秒钟之内就能完成！无论你的版本库是1个文件还是1万个文件。 

###### 创建与合并分支

**`master`分支是一条线，Git用`master`指向最新的提交，再用`HEAD`指向`master`，就能确定当前分支，以及当**
**前分支的提交点：（master===>最新提交     HEAD===>master）**
创+(name)切(switch -c name)删(-d)和(merge)查(branch)
查看分支：

```bash
git branch //branch 分支 git branch命令会列出所有分支，当前分支前面会标一个*号。
```

创建分支：

```
git branch <name>
```

切换分支：

```
git checkout <name> || git switch <name>
```

我们注意到切换分支使用`git checkout `，而前面讲过的撤销修改则是`git checkout -- `，同一个命令，有两种作用，确实有点令人迷惑。
实际上，切换分支这个动作，用`switch`更科学。因此，最新版本的Git提供了新的`git switch`命令来切换分支：
创建并切换分支：

```
git checkout -b <name>
git switch -c <name>
```

合并某分支到当前分支：

```
git merge <name> // merge 	合并, 融合, 并入
```

删除分支：

```
git branch -d <name>
```

强行删除分支

```
git branch -D <name> //要先合并
```

###### 解决冲突

- 当Git无法自动合并分支时，就必**须首先解决冲突。解决冲突后，再提交，合并完成**。

- **解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交**。

- 用`git log --graph`命令可以看到分支合并图。
	查看分支合并图

	```
	git log --graph // graph 图
	git log --graph --pretty=oneline --abbrev-commit
	```

###### 分支管理策略

合并分支时，加上`--no-ff`参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而`fast forward`合并就看不出来曾经做过合并。

###### Bug分支

- 修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；
- 当手头工作没有完成时，先把工作现场`git stash`一下，然后去修复bug，修复后，再`git stash pop`，回到工作现场；
- 在master分支上修复的bug，想要合并到当前dev分支，可以用`git cherry-pick `命令，把bug提交的修改“复制”到当前分支，避免重复劳动。
	每个bug都可以通过一个新的临时分支来修复，修复后，合并分支，然后将临时分支删除。
	Git还提供了一个`stash`功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作：

```
git stash
```

###### Feature分支

添加一个新功能时，你肯定不希望因为一些实验性质的代码，把主分支搞乱了，所以，每添加一个新功能，最好新建一个feature分支，在上面开发，完成后，合并，最后，删除该feature分支。

- 开发一个新feature，最好新建一个分支；

- 如果要**丢弃一个没有被合并过的分支**，可以通过`git branch -D `强行删除。

- 强行删除分支

	```
	git branch -D <name> //要先合并
	origin  git@github.com:michaelliao/learngit.git (fetch)
	origin  git@github.com:michaelliao/learngit.git (push)
	```

###### 多人协作

- 查看远程库信息，使用`git remote -v`；

	```
	git remote -v //更详细的信息
	origin  git@github.com:michaelliao/learngit.git (fetch)
	origin  git@github.com:michaelliao/learngit.git (push)
	```

	上面显示了可以抓取和推送的`origin`的地址。如果没有推送权限，就看不到push的地址。

- 本地新建的分支如果不推送到远程，对其他人就是不可见的；

- 从**本地推送分支**，使用`git push origin branch-name`，如果推送失败，先用`git pull`抓取远程的新提交。推送分支，就是把该分支上的所有本地提交推送到远程库。推送时，要指定本地分支，这样，Git就会把该分支推送到远程库对应的远程分支上：

	```
	git push origin branch-name  
	git add env.txt
	git add env.txt
	git push origin dev
	```

- 在**本地创建和远程分支对应的分支**，使用`git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；

	```
	git checkout -b branch-name origin/branch-name
	```

- **建立本地分支和远程分支的关联**，使用`git branch --set-upstream branch-name origin/branch-name`；

- 如果`git pull`提示`no tracking information`，则说明本地分支和远程分支的链接关系没有创建，用命令`git branch --set-upstream-to  origin/`。

	```
	 git branch --set-upstream-to=origin/dev dev
	git branch --set-upstream branch-name origin/branch-name
	```

- **从远程抓取分支**，使用`git pull`，如果有冲突，要先处理冲突。

	```
	git pull
	```

	你的小伙伴的最新提交和你试图推送的提交有冲突，解决办法也很简单，Git已经提示我们，先用`git pull`把最新的提交从`origin/dev`抓下来，然后，在本地合并，解决冲突，再推送：
	但是，并不是一定要把本地分支往远程推送，那么，哪些分支需要推送，哪些不需要呢？

- `master`分支是主分支，因此要时刻与远程同步；

- `dev`分支是开发分支，团队所有成员都需要在上面工作，所以也需要与远程同步；

- `bug`分支只用于在本地修复bug，就没必要推到远程了，除非老板要看看你每周到底修复了几个bug；

- `feature`分支是否推到远程，取决于你是否和你的小伙伴合作在上面开发。

###### Rebase

Git有一种称为rebase的操作，有人把它翻译成“变基”

- rebase操作可以把本地未push的分叉提交历史整理成直线；
- rebase的目的是使得我们在查看历史提交的变化时更容易，因为分叉的提交需要三方对比。

```
git log --graph --pretty=oneline --abbrev-commit
```

```
git rebase
```

- 分支管理解决的是什么问题
- 远程分支和本地分支
- 分支管理操作可以分类
- 分支命名规范

分支命名

- master 主分支
- develop 开发分支
- feature 开发新功能 
	- 命名规范 feature/开头的为特性分支 
		- /feature/user_module /feature/cart_module
- release
- hotfix

上传

```bash
git push 

git fetch --all  # → 将远程主机的更新全部取回本地

git pull origin master:master # → 将远程origin主机的master分支合并到当前master分支,冒号后面的部分表示当前本地所在的分支
```

拉取

```bash
git pull
```

查看分支

```bash
git branch  // 查看本地分支
git branch -r // 查看所有远程分支
git branch -a // 查看本地和远程分支
```

```
git branch -v 查看分支最后一个提交对象的信息
```

创建分支

```bash
git branch <name>
```

切换分支：

```bash
git checkout <name> || git switch <name>
```

创建+切换分支：

```bash
git checkout -b <name>git switch -c <name>

git branch -m brancholdname branchnewname # → 重命名分支
```

合并某分支到当前分支：

```bash
git merge <name> // merge 	合并, 融合, 并入
```

删除分支：

```bash
git branch -d<branchname> <name>

git branch -a 查看所有远程分支和本地分支

git push origin -d <branchname>   # → 删除远程branchname分支

git branch -m <oldbranch-name><newbranch-name>
```

强行删除分支

```bash
git branch -D <name> //要先合并
```

查看分支合并图

```bash
git log --graph // graph 图git log --graph --pretty=oneline --abbrev-commit

git fetch --p
更新分支

git branch --merged 查看哪些分支已经合并当前分支 
git branch --no-merged 查看哪些分支没有合并当前分支
```

```bash
git checkout -b 本地分支名x origin/远程分支名
```



## 标签管理

发布一个版本时，我们通常先在版本库中打一个标签（tag），这样，就唯一确定了打标签时刻的版本。将来无论什么时候，取某个标签的版本，就是把那个打标签的时刻的历史版本取出来。所以，标签也是版本库的一个快照。
Git的标签虽然是版本库的快照，但其实它就是指向某个commit的指针（跟分支很像对不对？但是分支可以移动，标签不能移动），所以，创建和删除标签都是瞬间完成的。
tag就是一个让人容易记住的有意义的名字，它跟某个commit绑在一起。

##### 创建标签

- 新建一个标签，默认为`HEAD`，也可以指定一个commit id；

	```
	git tag
	```

- 指定标签信息；

	```
	git tag -a -m "标签信息"
	```

- 指定标签信息；

	```
	git tag 
	```

##### 操作标签

- 推送一个本地标签；

	```
	git push origin
	```

- 推送全部未推送过的本地标签；

	```
	git push origin --tags
	```

- 删除一个本地标签；

	```
	git tag -d
	```

- 删除一个远程标签。

	```
	git push origin :refs/tags/
	```

#### 查找历史版本

```bash
//查找历史版本打标签 获取commit id值git log --pretty=oneline --abbrev-commit
```

#### 新建标签

```bash
git tag <tagname>  //新建一个标签，默认为HEAD，也可以指定一个commit id；git tag <tagname> <commit id>git tag v0.9 f52c633// git tag 标签 commit idgit tag v1.0
```

#### 查看所有标签

```bash
git tag
```

#### 查看标签信息(标签不是按时间顺序列出，而是按字母排序的)

```bash
git show <tagname>git show v0.1
```

#### 创建带有说明的标签

```bash
git tag -a <tagname> -m "标签信息"git tag -a v0.1 -m "version 0.1 released" 1094adb //用-a指定标签名，-m指定说明文字 commit id是f52c633
```

#### 推送一个本地标签；

```bash
git push origin <tagname>
```

#### 推送全部未推送过的本地标签；

```bash
git push origin --tags
```

#### 删除一个本地标签；

```bash
git tag -d <tagname>
```

#### 删除一个远程标签。（先删除本地标签，再到远程标签）

```bash
// 删除本地标签git tag -d <tagname>//删除远程标签git push origin :refs/tags/v0.9
```

查看远程库的远程主机

```bash
git remotegit remote -vorigin  git@github.com:michaelliao/learngit.git (fetch)origin  git@github.com:michaelliao/learngit.git (push)//origin 远程分支名
```

查看本地的分支信息

```bash
git branchmaster
```

怎么在远程仓库创建分支，直接在本地创建，然后push上去
上面显示了可以抓取和推送的`origin`的地址。如果没有推送权限，就看不到push的地址

#### 绑定远程分支

```
git branch --set-upstream branch-name origin/branch-name
```

#### 推送分支

```bash
git push <远程主机名> <本地分支名>:<远程分支名>git push origin mastergit push origin dev	git push -u origin master
```

#### 拉取分支

```bash
git pull <远程主机名> <远程分支名>:<本地分支名>
```

## 问题汇总

解决failed to push some refs to git

```bash
git pull --rebase origin master
```

 Git Push报错:remote: error: GH007: Your push would publish a private email address.

```bash
公开自已的邮箱Gitee 将保密你的邮箱地址，并在执行基于 Web | WebIde 的 Git 操作中，使用 5000737+code-dream@user.noreply.gitee.com 作为你的邮箱地址。如果你希望命令行 Git 操作使用你的私人邮箱地址，你必须在 Git 中设置你的邮箱地址。
```

 添加所有文件

```bash
git add .
```

.连接远程仓库

```bash
git remote add origin https://github.com/kong/springcloud.git 
```

访问私有仓库是必须保证远程仓库中有你的ssh
[remote: Incorrect username or password ( access token ) fatal: Authentication failed for - 编程361 - 博客园](https://www.cnblogs.com/sunmingduo/p/10055329.html)

```
gitee推送到远程仓库时提示错误remote: Incorrect username or password ( access token )fatal: Authentication failed for 'https://gitee.com/***/***.git/'
```

解决办法：清除本地的gitee用户名和密码
git config --system --unset credential.helper
再执行推送，重新输入用户名和密码。
error: failed to push some refs to 'git@github.com:heweiliang88/fast-learning-web.git'

```
// 对项目要先关联项目再更改内容要不然会报 failed to push some refs git clone git@github.com:heweiliang88/fast-learning-web.git git remote add github git@github.com:heweiliang88/fast-learning-web.git git add . git commit -m "v0.1"  ssh -T git@github.com git push github master git push  git push -f origin master // 强制更新
```

先同步远程库的内容，再把push上去问题

 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:heweiliang88/ASUSVivoBookS2-hackintosh.git'
hint: Updates were rejected because the remote contains work that you do

# Git图形化软件

Vscode 图形界面

基本使用Git

- 加号 添加到 暂存区
- 输入框 添加日志  打钩 提交日志
- 推送  分支 隔壁的 加载号

创建分支

- 点击master

- 上传分支 点击云

- 合并分支 

- 冲突  （云端与本地不一样）

# 忽略文件 .gitgnore

```
# 此为注释 – 将被 Git 忽略
# 忽略所有 .a 结尾的文件
*.a
# 但 lib.a 除外
!lib.a
# 仅仅忽略项目根目录下的 TODO 文件，不包括 subdir/TODO
/TODO
# 忽略 build/ 目录下的所有文件
build/
# 会忽略 doc/notes.txt 但不包括 doc/server/arch.txt
doc/*.txt
# 忽略 doc/ 目录下所有扩展名为 txt 的文件
doc/**/*.txt
```

# Github 高效搜索方法

```bash
in:name spring boot starts:>3000  forks:>2000
in:name React stars:>5000 forks:>2000
in:readme spring boot  starts > 3000  
in:description 微服务 language: java pushed:>2019-09-03
in:name xxx // 按照项目名搜索
in:readme xxx // 按照README搜索
in:description xxx // 按照description搜索

stars:>xxx // stars数大于xxx
forks:>xxx // forks数大于xxx
language:xxx // 编程语言是xxx
pushed:>YYYY-MM-DD // 最后更新时间大于YYYY-MM-DD
```

## github.io 的请求遭到拒绝

 .github.io 拒绝了我们的连接请求

- 原因：电信运营商 DNS 污染
- 解决方法：修改DNS服务器

插件

- Git History Diff 历史记录 

有如下几种解决方法：
1.使用强制push的方法：
$ git push -u origin master -f

2.push前先将远程repository修改pull下来
$ git pull origin master
$ git push -u origin master

3.若不想merge远程和本地修改，可以先创建新的分支：
$ git branch [name]
然后push
$ git push -u origin [name]

Source Tree 软件使用

Cloning into 'Mysuperweb'...
ssh: Could not resolve hostname gitee.com: Non-recoverable failure in name resolution
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

# xxx.github.io网站无法访问.md

## 问题原因

域名解析问题

## 解决方法

### 修改host文件

[查找网站对应的IP](https://ipchaxun.com )
host文件 `C:\Windows\System32\drivers\etc`

```bash
185.199.108.153 xxxxx.github.io
185.199.109.153 xxxxx.github.io
185.199.110.153 xxxxx.github.io
185.199.111.153 xxxxx.github.io
```

刷新网络DNS缓存

```bash
ipconfig /flushdns
```

### 科学加速的方法

### 修改DNS

使用 `DNS优选` 软件更换 DNS
成功

```
#
#127.0.01 localhost
#::1 localhost127.0.0.1 localhost
127.0.0.1 localhost
#::1 localhost
#::1 localhost
#127.0.0.1 registeridm.com
#127.0.0.1 www.registeridm.com
#127.0.0.1 www.internetdownloadmanager.com
#127.0.0.1:8083 www.heweiliang.com
#www.heweiliang.com 127.0.0.1:8083
#www.tplogin.cn 192.168.1.4
#192.168.1.4 www.tplogin.cn
#::1 localhost
#127.0.0.1 activate.navicat.com
#::1 localhost
#::1 localhost
#::1 localhost
::1 localhost
104.22.10.225 www.duboku.co
104.22.11.225 www.duboku.co
172.67.37.113 www.duboku.co
13.224.161.90 api.themoviedb.org
31.13.85.8 api.themoviedb.org
13.35.67.86 api.themoviedb.org
104.16.61.155 api.themoviedb.org
54.192.151.79 api.themoviedb.org
13.226.238.76 api.themoviedb.org
99.86.199.63 api.themoviedb.org
127.0.0.1  www.xmind.net
# GitHub Start 
192.30.255.112 gist.github.com
192.30.255.112 github.com
192.30.255.112 www.github.com
151.101.56.133 avatars0.githubusercontent.com
151.101.56.133 avatars1.githubusercontent.com
151.101.56.133 avatars2.githubusercontent.com
151.101.56.133 avatars3.githubusercontent.com
151.101.56.133 avatars4.githubusercontent.com
151.101.56.133 avatars5.githubusercontent.com
151.101.56.133 avatars6.githubusercontent.com
151.101.56.133 avatars7.githubusercontent.com
151.101.56.133 avatars8.githubusercontent.com
151.101.56.133 camo.githubusercontent.com
151.101.56.133 cloud.githubusercontent.com
151.101.56.133 gist.githubusercontent.com
151.101.56.133 marketplace-screenshots.githubusercontent.com
151.101.56.133 raw.githubusercontent.com
151.101.56.133 repository-images.githubusercontent.com
151.101.56.133 user-images.githubusercontent.com
185.199.108.153 xxxxx.github.io
185.199.109.153 xxxxx.github.io
# GitHub End
```

```
#
#127.0.01 localhost
#::1 localhost127.0.0.1 localhost
127.0.0.1 localhost
#::1 localhost
#::1 localhost
#127.0.0.1 registeridm.com
#127.0.0.1 www.registeridm.com
#127.0.0.1 www.internetdownloadmanager.com
#127.0.0.1:8083 www.heweiliang.com
#www.heweiliang.com 127.0.0.1:8083
#www.tplogin.cn 192.168.1.4
#192.168.1.4 www.tplogin.cn
#::1 localhost
#127.0.0.1 activate.navicat.com
#::1 localhost
#::1 localhost
#::1 localhost
::1 localhost
104.22.10.225 www.duboku.co
104.22.11.225 www.duboku.co
172.67.37.113 www.duboku.co
13.224.161.90 api.themoviedb.org
31.13.85.8 api.themoviedb.org
13.35.67.86 api.themoviedb.org
104.16.61.155 api.themoviedb.org
54.192.151.79 api.themoviedb.org
13.226.238.76 api.themoviedb.org
99.86.199.63 api.themoviedb.org
127.0.0.1  www.xmind.net
# GitHub Start 
192.30.255.112 gist.github.com
192.30.255.112 github.com
192.30.255.112 www.github.com
151.101.56.133 avatars0.githubusercontent.com
151.101.56.133 avatars1.githubusercontent.com
151.101.56.133 avatars2.githubusercontent.com
151.101.56.133 avatars3.githubusercontent.com
151.101.56.133 avatars4.githubusercontent.com
151.101.56.133 avatars5.githubusercontent.com
151.101.56.133 avatars6.githubusercontent.com
151.101.56.133 avatars7.githubusercontent.com
151.101.56.133 avatars8.githubusercontent.com
151.101.56.133 camo.githubusercontent.com
151.101.56.133 cloud.githubusercontent.com
151.101.56.133 gist.githubusercontent.com
151.101.56.133 marketplace-screenshots.githubusercontent.com
151.101.56.133 raw.githubusercontent.com
151.101.56.133 repository-images.githubusercontent.com
151.101.56.133 user-images.githubusercontent.com
185.199.108.153 xxxxx.github.io
185.199.109.153 xxxxx.github.io
140.82.113.3      github.com
140.82.114.20     gist.github.com
151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
199.232.68.133     avatars0.githubusercontent.com
199.232.28.133     avatars1.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
199.232.28.133     avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
199.232.68.133     avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
199.232.68.133     avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
199.232.68.133     avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
199.232.68.133     avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
199.232.68.133     avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com
199.232.68.133     avatars8.githubusercontent.com
199.232.68.133     raw.githubusercontent.com
199.232.68.133     user-images.githubusercontent.com
199.232.68.133     avatars2.githubusercontent.com
199.232.68.133     avatars1.githubusercontent.com
185.199.108.154               github.githubassets.com
199.232.68.133                camo.githubusercontent.com
52.168.24.190                 github.map.fastly.net
199.232.69.194                github.global.ssl.fastly.net
140.82.112.4                  github.com
140.82.112.5                  api.github.com
199.232.68.133                raw.githubusercontent.com
199.232.68.133                user-images.githubusercontent.com
199.232.68.133                favicons.githubusercontent.com
199.232.68.133                avatars5.githubusercontent.com
199.232.68.133                avatars4.githubusercontent.com
199.232.68.133                avatars3.githubusercontent.com
199.232.68.133                avatars2.githubusercontent.com
199.232.68.133                avatars1.githubusercontent.com
199.232.68.133                avatars0.githubusercontent.com
# GitHub End
```

# GitHub的README.md的svg图标

- [svg图标官网说明https://shields.io](https://shields.io/#/)
- [GitHub上 README 增加图片标签](https://blog.csdn.net/yangbodong22011/article/details/51791085)
- [简单图标库](https://simpleicons.org/)
  自动生成的方法
  [Shields.io: Quality metadata badges for open source projects](https://shields.io/)

```
前往网址Your BadgeStaticDynamic 动态
```

> `https://img.shields.io/badge/<图标前部分的文字>-<图标后部分的文字>-<颜色>.svg`
> `https://img.shields.io/static/v1?label=<LABEL>&message=<MESSAGE>&color=<COLOR>`
> 注意点：
> 1、因为-是会用到的分割字符，如果文字中有-，如要用--来代替，如Objective-C要写成Objective--C
> 2、颜色可以是支持的英文，也可以是6位的16进制的字符串，如blue、0000ff
> 3、可以支持圆角、矩形样式、社交样式、还可以添加logo
> MarkDown语法显示图片:  ![图片描述](D:/GitRepository/GithubProject/Blog/Blog/source/_posts/note/%E5%89%8D%E7%AB%AF/basic/js&&ts&&jq/%25E5%259B%25BE%25E7%2589%2587%25E9%2593%25BE%25E6%258E%25A5)
>
> ``![](https://img.shields.io/badge/download-1K-brightgreen.svg)``
> ![瘦小的圆角矩形](/Users/administrator/Workspace/编程/前端/basic/css/css&css3.assets/language-swift-brightgreen-1625065631467.svg)
> ![社交样式](D:/GitRepository/GithubProject/Blog/Blog/source/_posts/note/%25E5%2589%258D%25E7%25AB%25AF/basic/css/css&css3.assets/Stack_Overflow-10k+-red.svg)
> ![](/Users/administrator/Workspace/编程/Blog/Note/未发布/Git教程.assets/download-1K-brightgreen.svg)
> ![](/Users/administrator/Workspace/编程/前端/basic/css/css&css3.assets/npm-v3.2.0-blue-1625065631467.svg)![](https://img.shields.io/badge/npm-v3.2.0-blue.svg?style=flat-square)

```
![瘦小的圆角矩形](https://img.shields.io/badge/language-swift-brightgreen.svg?style=plastic)language-swift-brightgreenhttps://img.shields.io/badge/<图标前部分的文字>-<图标后部分的文字>-<颜色>.svgstyle=plastic 瘦小的圆角矩形style=flat-square 正常大小的矩形style=social 社交样式style=social&logo=github 带logo
```



# Github功能

## GIthub Action

> 开始使用 GitHub - GitHub Docs](https://docs.github.com/cn/get-started)
>
> [521xueweihan/GitHub520: 让你“爱”上 GitHub，解决访问时图裂、加载慢的问题。（无需安装）](https://github.com/521xueweihan/GitHub520)
>
> [gogs/gogs: Gogs is a painless self-hosted Git service](https://github.com/gogs/gogs)
>
> [pcottle/learnGitBranching：交互式 git 可视化和教程。 有抱负的 git 学生可以使用这个应用程序来教育和挑战自己对 git 的掌握！](https://github.com/pcottle/learnGitBranching)
>
> 一款极易搭建的自助 Git 服务。
>
> [anuraghazra/github-readme-stats: Dynamically generated stats for your github readmes](https://github.com/anuraghazra/github-readme-stats)
>
> 在你的 README 中渲染动态生成的 GitHub 统计信息！
>
> [521xueweihan/HelloGitHub: 分享 GitHub 上有趣、入门级的开源项目。Share interesting, entry-level open source projects on GitHub.](https://github.com/521xueweihan/HelloGitHub)
>
> [GitHubDaily/GitHubDaily: 坚持分享 GitHub 上高质量、有趣实用的开源技术教程、开发者工具、编程网站、技术资讯。A list cool, interesting projects of GitHub.](https://github.com/GitHubDaily/GitHubDaily)
>
> [GitHub资源 · GitHub秘籍（中文版） · 看云](https://static.kancloud.cn/thinkphp/github-tips/37901)
>
> [github-cheat-sheet/README.zh-cn.md at master · tiimgreen/github-cheat-sheet](https://github.com/tiimgreen/github-cheat-sheet/blob/master/README.zh-cn.md)
