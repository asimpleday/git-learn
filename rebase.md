# git rebase
## 概述
`git rebase` 命令可以对某一段线性提交历史进行编辑、删除、复制、粘贴，因此，合理使用rebase命令可以使我们的提交历史干净、简洁。
## 用法
1、当我们在本地仓库中提交了很多次，在我们把本地提交push到公共仓库中之前，为了让提交记录更简洁明了，我们希望把如下分支B、C、D三个提交记录合并为一个完整的提交，然后再push到远程仓库。

![](https://upload-images.jianshu.io/upload_images/2147642-42195cacced56729.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/417/format/webp)

下面是具体提交历史：

![](https://upload-images.jianshu.io/upload_images/2147642-ce849c4eab3d803b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/434/format/webp)

这里我们使用命令：
```
git rebase -i [startpoint] [endpoint]
```
其中 `-i`的意思是 `--iinteractive`，即弹出交互式的界面让用户编辑完成合并操作， `[startpoint]`、`[endpoint]`则指定了一个编辑区间，如果不指定`[endpoint]`，则该区间的终点默认是当前分支HEAD所指向的`commit`(注：该区间指定的是一个前开后闭的区间)。在查看到了log日志后，我们运行以下命令：
```
git rebase -i 36224db
```
然后我们会看到如下界面：

![](https://upload-images.jianshu.io/upload_images/2147642-03d48aa767efb307.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/647/format/webp)

上面未被注释的部分列出的是我们本次rebase操作包含的所有提交，下面注释部分是git为我们提供的命令说明，每一个commit id前面的 `pick`表示指令类型，git为我们提供了以下几个命令：
- pick： 保留该commit(缩写：p)
- reword： 保留该commit，但我需要修改该commit的注释(缩写：r)
- edit： 保留该commit，但我要停下来修改该提交，不仅仅是修改注释(缩写：e)
- squash： 将该commit和前一个commit合并(缩写：s)
- fixup： 将该commit和前一个commit合并，但我不要保留该提交的注释信息(缩写：f)
- exec： 执行shell命令(缩写：x)
- drop： 我要丢弃该commit(缩写：d)

根据需求，我们将commit内容编辑如下：

![](https://upload-images.jianshu.io/upload_images/2147642-a651234e62ed20a5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/536/format/webp)

然后是注释修改界面：

![](https://upload-images.jianshu.io/upload_images/2147642-44bbd784dcadfb31.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/801/format/webp)

编辑完保存即可完成commit的合并了：

![](https://upload-images.jianshu.io/upload_images/2147642-334e0a5c47a24f87.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/448/format/webp)
