# git diff
## 概述
`git diff`命令用来文件之间的差异，比如工作区中的a.txt和暂存区中的a.txt有什么变化。
## 用法
```
# 查看工作区和暂存区的差异

git diff
```
```
# 查看某个文件工作区和暂存区的差异

git diff <fileName>
```
```
# 查看暂存区与版本库中当前commit的差异

git diff --cached
```
```
# 查看俩个commit的差异
# 这里要把之前的提交id放到前面才能看到当前的提交相对于之前的提交变化了什么

git diff <commitBeforeId> <commitAfterId>
```
```
# 查看工作区与当前commit的差异

git diff HEAD


# 查看工作区与上一次commit的差异

git diff HEAD^
```
```
# 查看工作区和某次commit的差异

git diff <commitId>
```