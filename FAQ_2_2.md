## 配置本地git环境

请从Git官网下载最新版的[Git客户端](http://git-scm.com/downloads)。（注，请自备纵云梯）

安装完客户端后，需要完成以下的配置：


**配置用户名**

确认你在CSDN id,获取的方式是在登录后，进入my.csdn.net，在您的个人头像图片右侧，昵称信息上方的粗体字即为用户名。

获知用户名后，在命令行中输入：

	git config --global user.name "CSDN id"


**配置邮箱**

配置的Git邮箱应与CSDN passport中注册邮箱一致，系统判断用户名是依靠邮箱信息：

	git config --global user.email "CSDN passport中注册邮箱"


**检查配置**

最后检查user.name及user.email是否配置正确：

	git config -l