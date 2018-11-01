# git reset
## 概述
`git reset`用来进行回撤操作
## 用法
#### 从版本库撤回到暂存区
```
# 回到HEAD之前的那个commit，回撤到暂存区，不会重置暂存区

git reset HEAD^ --soft
```
```
# 回撤提交，重置工作区、暂存区

git reset HEAD --hard
```
#### 从暂存区撤回到工作区
```
# 全部撤回到工作区

git reset
```
```
# 撤回到工作区,不会重置工作区

git reset --soft
```
```
# 撤回到工作区,会重置工作区

git reset --hard
```
#### 何为重置？
举个例子：

1、新建了一个 a.txt 文件，写入内容111。

2、`git add a.txt`提交到暂存区。

3、工作区继续修改 a.txt 文件，写入内容222。

分析：到此时暂存区里的 a.txt 文件内容为 111，而工作区的 a.txt 文件内容为111 222

4、执行撤回操作,这里有俩个方案

4.1、 `git reset --soft` 不会重置工作区，所以 `cat a.txt`查看文件的内容，是 111 222

4.2、`git reset --hard` 会重置工作区，所以 `cat a.txt`查看文件的内容，是 111
