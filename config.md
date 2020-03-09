## git add 时因为换行符导致的警告信息清除
提交时转换为LF，检出时转换为CRLF，默认设置不用修改，Git是linux配置
```
git config --global core.autocrlf true
```

允许提交包含混合换行符的文件
```
git config --global core.safecrlf false
```
