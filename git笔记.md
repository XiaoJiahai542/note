## 仓库地址：

https://github.com/XiaoJiahai542/note.git

##  配置

创建空目录：mkdir 名称

进入项目目录：cd  名称

git初始化：git inti（表现为：会在项目目录下创建”.git“的隐藏目录，该目录不能删除，也不能随意更改。）

![image-20200309212800450](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212800450.png)



## 文件添加与注释

查看当前状态：git status

添加到缓存区：git add 文件名

- 语法1：git add 文件名（添加一个文件）

- 语法2：git add 文件名1 文件名2 文件名3 ……（添加多个文件）

- 语法3：git add.（添加当前目录到缓存区中）

  【若不想打文件名，可以直接用语法三】

提交至版本库：git commit -m “注释内容”（注释可以写中文）

![image-20200309212853305](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212853305.png)



## 时光穿梭机——版本回退

确定需要回到的时间点

- 语法1：git log（执行的结果为显示日志）
- 语法2：git log --pretty=oneline（较语法1更为简洁）

回退操作指令：git reset --hard 提交编号

![image-20200309212951392](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212951392.png)

//若是回退到过去以后又想回到回退之前，便可用指令“git reflog”去查看历史操作以得到编号，再用   回退操作指令   回到回退之前即可。

删除文件

- 语法：

  ~~~
  $rm 文件名					//从工作区删除该文件
  $git rm 文件名				//从版本库删除该文件
  rm '文件名'
  
  $git checkout --文件名		//若是删错了文件，可以用此指令撤销
  ~~~

  git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”





## 远程仓库的使用

使用clone指令克隆线上仓库到本地

- 语法：git clone 线上仓库地址

在仓库上做对应操作（提交暂存区、提交本地仓库、提交线上仓库、拉取线上仓库）

- 提交线上仓库指令：git push/git push -u origin master

- 拉取线上仓库指令：git pull



## 分支相关指令

- 查看分支：git branch	（当前分支前又“*”标记）
- 创建分支：git branch 分支名
- 切换分支：git checkout 分支名
- 删除分支：git branch -d 分支名（在删除分支时，一定要退出被删除分支，否则不能删除）
- 合并分支：git merge 被合并的分支名
- 对于新分支，可以使用“git checkout -b 分支名”指令，相当于创建并切换到此分支。



## 标签

git tag 标签名      （创建一个新标签）

git tog       			（查看当前所有标签）

git tag 标签名 其commit id       （对某次提交打标签）

git tag -d 标签名      （删除标签）

​		如果某次标签已经推送至远程，在删除本地标签以后还需删除远程标签：git push origin :refs/tags/标签名

git push origin 标签名      （将此标签推向至远程）

git push origin –tag     	（将还未推送至远程的所有标签推送至远程）

## 忽略文件

忽略文件需新建一个名为“.gitignore”的文件，该文件用于忽略文件或不忽略文件的规则。**该规则对当前目录及其子目录生效**。

该文件无法直接在Windows目录下直接创建，需用命令行Git Bash来touch创建。

一些常规写法

1. /mtk/      过滤整个文件
2. *.zip        过滤掉所有.zip文件
3. /mtk/do.c    过滤某个具体文件
4. lindex.php    不过滤具体某个文件



## 配置别名

语法：git config --global alias.所配置的名称 被配置指令名称

例如：

~~~
git config --global alias.st status		//以后要敲git status时，只用敲git st就行
~~~



遇到问题：之前敲  git commit -m ’注释内容‘   指令的时候少打了个空格。

解决方法：经过多次尝试以后发现m后面要敲空格。

遇到问题：最初提交线上仓库的时候用“git push”命令需要输入两次用户名和密码，但是还是登陆不上去。

解决方法：去网上百度以后用“git push -u origin master”代替”git pull”,然后输入一次用户名和密码就可以了。





感想：这一两天主要是在B站根据视频学的git，学的时候是比较痛苦的，因为git和GitHub是全英文的，所以即使是一些指令和错误我都看不懂，只能把百度翻译放在一旁，边翻译边学习，通过不懈努力终于还是把git学习内容粗略的过了一遍。通过这次对git的学习与了解，觉得它是一个很重要的办公软件，对以后学习和工作都会提供一定的帮助。我还下载了GitHub Desktop这个软件，然而它是全英的，根本看不懂，所以此时此刻觉得英语真的是一门非常非常重要的语言。