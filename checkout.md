# git checkout
## 概述
`git checkout`命令可以用来撤销本地的修改

## 用法
#### 撤销指定文件

```
## 撤销当前文件下的abc.txt文本文件
git checkout -- abc.txt

## 撤销a文件夹下的abc.txt文本文件
git checkout -- a/abc.txt
```
#### 撤销所有文件的修改

```
git checkout .
```