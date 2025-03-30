# git bash

```
cd ..\          #返回上一级目录
git init     repo   #在本目录下创建repo这个空文件夹
echo "file1" >  file1.txt  #创建文件
git add file.txt   #把文件file.txt文件从工作区提交到缓存区
git add *.txt   #把txt文件都转为缓存区
git  add .      #把所有文件都添加到暂存区
git commit -m  "这是第n次提交"  #文件从缓存区提交到库中
git commit      #不输入-m就会进入vim界面   先按i进入信息编辑模型，》esc》：wq退出保存
git  status     #查看状态
git log         #查看提交记录
git  log --oneline  #查看简介的提交记录
```

## 文件复制

```
cp -rf repo repo-hard  #复制文件repo名为repo-hard
```

## 查看工文件

```
ls    #查看工作区文件
git ls-files  #查看暂存区文件
```

## 回退版本

```
git reset --soft   #工作区和暂存区都保留
git reset --hard   #工作区和暂存区都不保留
git reset --mixed  #工作区保留暂存区不保留
```

## 查看历史记录

```
git reflog   
```

## git diff

1.查看工作区，缓存区，本地仓库之间的差异

2.查看不同版本之间的差异

3.查看不同分支的差异

```
vi file3.txt   #打开文件修改文件内容
git  diff HEAD #比较工作区和版本库之间的差异
git diff --cached  #比较暂存区和版本库之间的差异
git diff a54094c  637023e #查看两个版本的差异内容
git diff HEAD a54094c #HEAD(最新版本)和目标版本的差异内容
git diff HEAD~ HEAD   #比较当前版本和上一个版本之间的差异
git diff HEAD~2 HEAD  #比较当前版本和之前两个版本之间的差异
git diff HEAD~2 HEAD file3.txt ##比较当前版本和之前两个版本之间的差异,只查看file3.txt这个文件的差异内容
```

# 使用git rm 删除文件

```
ls -ltr              #显示本地文件
git ls-files         #查看暂存区的内容
git rm file1.txt     #不仅删除了工作区的文件而且删除了暂存区的文件
```

# .gitignore忽略文件

应该忽略哪些文件：

1.系统或软件自动生成的文件

2.编译产生的中间文件和结果文件

3.运行时生成日志文件，缓存文件，临时文件

4.涉及身份，密码，口令，密钥等敏感信息文件

# 一般流程

```
#1.初始化本地仓库
git init
#2.关联远程仓库
git remote add origin https://github.com/用户名/仓库名.git
#3.拉取远程变更
git pull origin main
#4.创建切换分支
git checkout -b 新分支
#5.开发修改
git status
#6.提交到本地仓库
git add .               #添加所有修改
git commit -m "提交描述" #提交到本地
#7推送至GitHub
git push orgin 分支名
```

