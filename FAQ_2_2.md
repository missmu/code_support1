## 配置本地git环境

请从Git官网下载最新版的[Git客户端](http://git-scm.com/downloads)。注，请自备纵云梯

安装完客户端后，需要完成以下的配置：

- **配置用户名**

确认你在CSDN id,获取的方式是在登录后，屏幕右上角图标即是CSDN id

![](/CSDN_Code/code_support/blob/master/images/FAQ_2_2_1.png.png)

然后在命令行中输入
>`git config --global user.name "CSDN id"`


- **配置邮箱**

配置的Git邮箱应与CSDN passport中注册邮箱一致，系统判断用户名是依靠邮箱信息。
>`git config --global user.email "CSDN passport中注册邮箱"`

- **检查配置**

最后检查配置
>`git config -l`

检查user.name及user.email是否配置正确