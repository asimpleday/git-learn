# git blame
## 概述
查看文件的每一行是谁修改的，会得到整个文件的每一行的详细修改信息：包括SHA串、作者、日期、每一行内容。
## 用法
```
git blame [fileName]
```
```
# 加上 -L 参数在命令中指定开始行和结束行(包括开始行和结束行)

git blame -L 2,4 [fileName]
```
