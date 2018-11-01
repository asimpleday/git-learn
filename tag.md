# git tag
## 概述
`git tag`命令用于在 commit 上定义一个标签
## 用法
```
# 在当前 commit 上，定义一个标签

git tag [tagName]
```
```
# 在当前 commit 上，定义一个标签，并给具体注释信息

git tag [tagName] -m "message"
```
```
# 在某个commit上，定义一个标签

git tag [tagName] [commitId]
```
```
# 列出所有标签

git tag
```
```
# 把某个标签删除掉

git tag -d [tagName]
```
## 注意点
提交到远程仓库时并不会把tag推送上去，需要手动提交
```
# 把所有的标签提交到远程仓库

git push origin --tags
```
```
# 把某个标签提交到远程仓库

git push origin [tagName]
```