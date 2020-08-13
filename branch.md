# git branch
## 概述
`git branch` 是分支操作命令
## 用法
```
# 列出所有本地分支

git branch
```
```
# 列出所有本地分支和远程分支

git branch -a
```
```
# 新建一个分支，依旧停留在当前分支

git branch [branchName]
```
```
# 切换分支

git checkout [branchName]
```
```
# 新建一个分支，并切换到该分支

git checkout -b [newBranch]
```
```
# 删除分支，如果该分支没有未合并的变动

git branch -d [branchName]
```
```
# 删除分支，强制删除，不管有没有未合并变化

git branch -D [branchName]
```
```
# 分支改名

git checkout -b [newBranchName] [oldBranchName]
git branch -d [oldBranchName]
```
```
# 分支合并

git merge [branchName]
git branch -d [branchName]
```

```
# 删除远端分支

git push origin :dev
```

