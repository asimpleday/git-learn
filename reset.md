# git reset
## 概述
`git reset`用来进行回撤操作
## 用法
#### 从版本库撤回到暂存区
```
回到HEAD之前的那个commit，回撤到暂存区，不会重置暂存区

git reset HEAD^
```
```
# 版本库回到HEAD之前的那个commit，回撤到暂存区，不会重置暂存区

git reset HEAD^ --soft
```
#### 从暂存区撤回到工作区

```
# 撤回到工作区,不会重置工作区

git reset --soft （有疑问）
```
```
# 把指定文件撤回，不会覆盖工作区  √

git reset head aaa.txt
```

```
# 把所有文件撤回，不会覆盖工作区 √

git reset head

# 也可简写为如下 √

git reset
```

#### 从版本库撤回到工作区

```
# 完全重置为和HEAD的新位置相同的内容，换句话说，就是你的没有commit的修改会被全部擦掉（但不会擦除新添加的文件 Untracked files 未被监视）

git reset head --hard

# 可以简写为如下

git reset --hard

# 回到具体某一次提交的状态

git reset e66cf96 --hard
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
