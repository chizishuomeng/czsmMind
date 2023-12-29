## Git工作流程

**一般工作流程**
- 克隆git资源作为工作目录
- 在克隆的资源上添加或修改文件
- 如果其他人修改了，你可以更新资源
- 在提交前查看修改
- 提交修改
- 在修改完成后，如果发现错误，可以撤回提交并再次修改并提交

## Git工作区，暂存区和版本库

**基本概念**
- 工作区：就是在电脑上能够看到的目录
- 暂存区：一般存放在`.git`目录下的index文件中，所以我们把暂存区有时候又叫索引
- 版本库：工作区有一个隐藏的目录`.git`，这个不算工作区，而是git的版本库

## Git常用命令

```shell
## 全局配置
git config --global user.name "czsm"
git config --global user.email "2209924865@qq.com"
## 查看配置信息
git config --list


## 创建仓库
git init ## 在当前文件夹下创建仓库
git init newrepo ## 指定文件下创建仓库
## 将文件添加到暂存区
# git add 是告诉git开始对这些文件进行跟踪
git add . # 添加全部文件
git add 指定文件名 # 添加指定文件添加
# 提交
git commit -m "提交信息"

## 克隆仓库，将远程仓库拉取到本地
git clone 远程仓库地址

## 提交与修改
git add # 将文件添加到暂存区
git status # 查看仓库当前状态，显示有变动的文件
git diff # 比较文件的不同，即暂存区与工作区之间的差异
git commit # 提交暂存区的文件到本地仓库
git reset # 回退版本
git rm # 将文件从暂存区和工作区中删除
git mv # 移动或重命名工作区的文件
git checkout # 切换分支
git switch # 更清晰的切换分支
git restore # 恢复或撤销文件的更改

## 提交日志
git log # 查看提交日志
git blame 文件名 # 以列表形式查看指定文件的历史修改记录

## 远程操作
git remote # 远程仓库操作
git fetch # 从远程获取代码库
git pull # 下载远程代码并合并
git push # 上传远程代码并合并
```