创建空目录：mkdir 名称

进入项目目录：cd  名称

git初始化：git inti（表现为：会在项目目录下创建”.git“的隐藏目录，该目录不能删除，也不能随意更改。）

![image-20200309212800450](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212800450.png)



git常用指令操作

查看当前状态：git status

添加到缓存区：git add 文件名

- 语法1：git add 文件名（添加一个文件）

- 语法2：git add 文件名1 文件名2 文件名3 ……（添加多个文件）

- 语法3：git add.（添加当前目录到缓存区中）

  【若不想打文件名，可以直接用语法三】

提交至版本库：git commit -m “注释内容”（注释可以写中文）

![image-20200309212853305](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212853305.png)



时光穿梭机——版本回退

确定需要回到的时间点

- 语法1：git log（执行的结果为显示日志）
- 语法2：git log --pretty=oneline（较语法1更为简洁）

回退操作指令：git reset --hard 提交编号

![image-20200309212951392](C:\Users\xiaoj\AppData\Roaming\Typora\typora-user-images\image-20200309212951392.png)

若是回退到过去以后又想回到回退之前，便可用指令“git reflog”去查看历史操作以得到编号，再用   回退操作指令   回到回退之前即可。





远程仓库的使用

使用clone指令克隆线上仓库到本地

- 语法：git clone 线上仓库地址

在仓库上做对应操作（提交暂存区、提交本地仓库、提交线上仓库、拉取线上仓库）

- 提交线上仓库指令：git push -u origin master（第一次输入）

  ​									git push（第二次及以后输入）

- 拉取线上仓库指令：git pull





