# git commit
## 概述
`git commit`命令用来将暂存区中的变化提交到版本库
## 用法
`-m`参数是必须的，用来指定commit信息，如果不填，会打开文本编辑器，要求输入。

```
git commit -m "message"
```
```
# 直接把工作区中的变化提交到版本库,前提是版本库必须要有此次提交文件的版本历史

git commit -am "message"

```