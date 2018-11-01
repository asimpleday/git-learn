# git remote
## 概述
添加远程库
## 用法
```
# 查看关联的远程仓库的名称

git remote
```
```
# 查看关联的远程仓库的详细信息

git remote -v
```
```
# 本地仓库与远程仓库进行连接

git remote add origin [url]
```
```
# 列出某个主机的详细信息

git remote show name
```
## 注意
如果需要修改远程仓库地址，方法有三种
```
# 修改命令

git remote set-url origin [url]
```
```
# 先删后加

git remote rm origin
git remote add origin [url]
```
```
# 直接修改config文件

cd .git
vim config
```
