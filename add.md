# git add
## 概述
`git add`命令用于将工作区变化的文件，提交到暂存区，它的作用就是告诉git，下一次哪些变化需要保存到版本库。
## 用法
```
# 将指定文件放入暂存区

git add <file>  
```
```
# 将当前目录所有变化过的文件放入暂存区

git add .   
```
```
# 将指定目录下有变化的文件放入暂存区

git add <directory>  
```
## 详细参数
`-u`参数表示只添加暂存区已有的文件（包括删除操作），但不添加新增的文件。
```
git add -u
```
`-A`或者`-all`参数等同于`git add .`
```
git add -A
git add --all
```
`-f`参数表示强制添加某个文件，不管.gitignore是否包含了这个文件。
```
git add -f <fileName>
```