## 推荐一个git辅助工具：TortoiseGit 

对于很多不熟悉git命令的朋友来说，使用git命令行操作简直太难了。

这里我们推荐一个辅助工具，TortoiseGit，它可以把一些常用的git操作转换为可视化操作，让你不用再记忆大量git命令。

[TortoiseGit下载地址：](https://code.google.com/p/tortoisegit/wiki/Download?tm=2)

安装好TortoiseGit后，你会发现鼠标右键多了许多git操作菜单。如图：

![](/images/TortoiseGit.jpg)

现在我们来看一个基本的git项目提交操作是如何在TortoiseGit帮助下完成的。

假设你已经为一个git项目做好了修改，现在需要push到CODE平台上去了。

在项目所在文件夹，点击右键（你会发现右键菜单比刚刚未在git项目中时多了一些项目）。

![](/images/TortoiseGit_2.jpg)

(1) 选择“Git Add all files now”，这一步是将文件添加到git库中，相当于 "git add" 命令

(2) 选择“Git Commit Tool”，这一步相当于“git commit”命令

(3) 在弹出的对话窗口，你会看到刚刚改动过的项目文件都在左侧显示，前面还有对勾等标志。这些是待提交的文件。在右侧的文本框中加入你本次提交的说明，点击“提交按钮”。这一步相当于git命令的“git -m”
![](/images/TortoiseGit_3.jpg) 

(4)打开git bash，进行最后一步：输入 git push命令，将项目改动推送到CODE平台。