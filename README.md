# Git 基本操作手顺

> 通过TortoiseGit操作和通过命令行操作。


## 克隆代码

### 取得克隆地址

测试用仓库地址：`https://github.com/PetrichorSyu/gitnoob-guide.git`

![](image/image.png "")



### 克隆

#### TortoiseGit

![](image/image_1.png "")

![](image/image_2.png "")

![](image/image_3.png "")



#### 命令行

![](image/image_4.png "")



![](image/image_5.png "`[git clone https://github.com/PetrichorSyu/gitnoob-guide.git](https://github.com/PetrichorSyu/gitnoob-guide.git)`")

![](image/image_6.png "")

## 创建作业用分支，提交，推送

#### TortoiseGit

![](image/image_7.png "")

![](image/image_8.png "建议：分支名根据作业内容命名，如画面名，技能名
勾选Switch to new branch：直接切换到创建的分支 ")

![](image/image_9.png "")

![](image/image_10.png "作成文件test1.txt，确认提交分支。")

![](image/image_11.png "确认提交分支是否正确
双击修改文件列表，可查看修改内容")

![](image/image_12.png "Push：推送代码到远程分支")

![](image/image_13.png "")

![](image/image_14.png "")

![](image/image_15.png "可网页确认分支信息")

#### 命令行

![](image/image_16.png "git status：确认本地仓库信息
git add：添加修改文件至暂存区（可使用【git add .】添加所有修改文件 ）
git commit：提交暂存区修改内容至本地仓库
git push：推送本地仓库至远程仓库（第一次可能需要创建本地仓库和远程仓库的链接）")

## 合并作业分支至主分支

这里只介绍一种方法，通过网页创建`pull request`。

![](image/image_17.png "")

![](image/image_18.png "")

![](image/image_19.png "确认PR的提交信息，指定review担当者。")

![](image/image_20.png "File changed：方便leader review代码。
确认没有问题后，可 Merge pull request至主分支。

")

![](image/image_21.png "")

## 合并主分支最新代码至个人分支

假定主分支以下变更：

`test1.txt` 第一行有更新

`test2.txt` 最后一行有更新

`test3.txt` 新建

![](image/image_22.png "")

假定个人分支以下变更：

`test1.txt` 第一行有更新

`test2.txt` 第一行有更新

`test4.txt` 新建

![](image/image_23.png "")

### 从主分支取得代码

![](image/image_24.png "")

![](image/image_25.png "更改为想要取得代码的分支
等同于命令： git pull origin main")

![](image/image_26.png "文件冲突（若没有冲突，会自动merge）")

![](image/image_27.png "")

### 冲突解决

![](image/image_28.png "")

![](image/image_29.png "双击冲突文件，查看信息。（test2-4.txt 已自动merge，此处不显示）")

![](image/image_30.png "左上：远程分支更改内容
右上：本地分支更改内容
中下：merge后的文件内容，可右键冲突位置，执行相关操作。")

![](image/image_31.png "")

![](image/image_32.png "冲突解决后，各文件状态。")

### ※冲突解决后代码提交※

根据项目经验，此处很容易出错。（一般会根据svn使用经验，revret掉不是自己的代码，这样做是错误的！切记！）可确认下TortoiseGit的提醒信息！

根据项目经验，此处很容易出错。（一般会根据svn使用经验，revret掉不是自己的代码，这样做是错误的！切记！）可确认下TortoiseGit的提醒信息！

根据项目经验，此处很容易出错。（一般会根据svn使用经验，revret掉不是自己的代码，这样做是错误的！切记！）可确认下TortoiseGit的提醒信息！

![](image/image_33.png "")



![](image/image_34.png "这是git生成的merge履历，点击commit时会提醒提交信息中含有Conflicts信息。（个人认为可以删除Conflicts信息也可以忽略）")

![](image/image_35.png "")

Commit后再执行push操作，推送至个人远程分支。

![](image/image_36.png "")

![](image/image_37.png "创建Pull request，确认个人分支和主分支的区别。（！此处显示的都是自己修改的内容！）")

## 操作杂项

### 切换分支

![](image/image_38.png "等同于： git checkout <branch name>")

### 取得代码

![](image/image_39.png "等同于：git pull")

### 推送代码到远程分支

![](image/image_40.png "等同于：git push")

### 查看提交履历

![](image/image_41.png "")



