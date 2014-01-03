## 使用前的准备

CODE平台是一个使用git版本管理工具的代码托管与社交编程平台，很多与你本机交互的工作都需要用到git工具，所以我们强烈建议您在使用之前先配置本地git环境。

按照以下步骤操作：

### 1、[配置git环境](/help/CSDN_Code/code_support/FAQ_2_2)

请从Git官网下载最新版的[Git客户端](http://git-scm.com/downloads)。（注，请自备纵云梯）

安装完客户端后，需要完成以下的配置：


**配置用户名**

确认你在CSDN id,获取的方式是在登录后，进入passport.csdn.net，在“个人帐号”的最下端查看用户名：

![](/images/FAQ_2_2_1.png)

然后在命令行中输入：

	git config --global user.name "CSDN id"


**配置邮箱**

配置的Git邮箱应与CSDN passport中注册邮箱一致，系统判断用户名是依靠邮箱信息：

	git config --global user.email "CSDN passport中注册邮箱"


**检查配置**

最后检查user.name及user.email是否配置正确：

	git config -l

### 2、[添加SSH公钥](/help/CSDN_Code/code_support/FAQ_2_3)



公钥是CODE识别您的用户身份的一种认证方式，通过公钥，您可以将本地git项目与CODE建立联系，然后您就可以很方便的将本地代码上传到CODE，或者将CODE代码下载到本地了。

以下介绍生成公钥和管理公钥的方法。如果你是在windows系统下使用，需要先安装git的windows客户端[msysgit](http://code.google.com/p/msysgit) ,  然后运行 Git Bash, 在弹出的终端中输入下面提示的代码。


**生成公钥**

首先检查本机公钥：

	$ cd ~/.ssh
 
如果提示：No such file or directory 说明你是第一次使用git。如果不是第一次使用，请执行下面的操作,清理原有ssh密钥。

	$ mkdir key_backup
	$ cp id_rsa* key_backup
	$ rm id_rsa*

生成新的密钥：

	$ ssh-keygen -t rsa -C “您的邮箱地址”
 
在回车中会提示你输入一个密码，这个密码会在你提交项目时使用，如果为空的话提交项目时则不用输入。
 
您可以在你本机系统盘下，您的用户文件夹里发现一个.ssh文件，其中的id_rsa.pub文件里储存的即为刚刚生成的ssh密钥。

**添加公钥**

登录CODE平台，进入用户“账户设置”，点击右侧栏的“ssh公钥管理”，点击“添加公钥”，将刚刚生成的公钥填写到“公钥”栏，并为它起一个名称，保存即可。

**注意**：复制公钥时不要复制多余的空格，否则可能添加不成功。

### 3、推荐一个git辅助工具：TortoiseGit

* [下载地址](https://code.google.com/p/tortoisegit/wiki/Download?tm=2)  
* [使用介绍](/help/CSDN_Code/code_support/new_10)  