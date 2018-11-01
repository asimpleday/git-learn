# git rm
## 概述
已经提交到版本库，从工作区删除文件
## 用法
```
# 删除完需要进行一次提交

git rm hello.txt
git commit -m "删除了hello.txt文件"
```
## 注意
`git rm` 与 `rm` 的区别

用 `git rm` 来删除文件，同时还会将这个删除操作记录下来，用 rm 来删除文件，仅仅是删除了物理文件，没有将其从 git 的记录中删除。

直观的说，`git rm` 删除过的文件，执行 `git commit -m "hello.txt"` 提交时，会自动将删除该文件的操作提交上去。

而 `rm` 删除后，需要使用 `git add hello.txt` ，然后再 `git commit -m "hello.txt"`，才会将删除文件的操作提交上去。
