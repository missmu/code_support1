## 我想同时维护两个git托管平台的项目

如果你的项目同时托管在了两个git平台上（比如github和CODE），想同步维护两个平台上的同一个项目，也是很方便的。

### 1、设置账号绑定



### 2、git pull和git push

为了保持本地项目处于最新状态，建议您在每次修改项目之前都是用git pull命令将云端的代码“拉回”一份回来，修改后在push回去。

根据绑定账号时的设置，从两个平台回拉和推送代码的语法将分别是：

>git pull github master  从github回拉
 
>git pull code master  从CODE回拉

>git push github master  推送到github

>git push code master    推送到CODE

### 3、CODE平台的自动同步功能

如果你仅将CODE平台作为github项目的镜像站，而不打算在上面做任何独立提交和更新，可以使用CODE平台的“自动同步功能”。

* 该功能只支持git版本管理项目   
* 该功能使用的是--force模式，在CODE平台上的所作改动将被清除。  
* 在CODE平台的操作不能被逆向同步到github等网站  

由于自动同步这一功能的危险性和比较占用系统资源，如果您确实需要这一功能，请***发送邮件到codesupport@csdn.net**，注明您项目的github地址和CODE地址，申请开通自动同步。