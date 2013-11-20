## 我想同时维护两个git托管平台的项目

如果你的项目同时托管在了两个git平台上（比如github和CODE），想同步维护两个平台上的同一个项目，也是很方便的。

### 1、设置账号绑定

我们预设使用场景是用户已经使用github为主要协作平台，CODE平台为同步平台

首先你需要在两个平台上都添加上同一份公钥。关于如何生成和添加公钥请参看CODE帮助[管理公钥](/help/CSDN_Code/code_support/FAQ_2_3)

添加完公钥后，需要在命令行中配置git账号的信息。两个平台最好使用同样的用户名和注册邮箱。如果注册邮箱不同，你可以把CODE的注册邮箱添进github的邮箱列表（github支持一个账号绑定多个邮箱）。

以下是设置账号的git命令：

`git config set user.name` 设置绑定用户名，此处可以与平台用户名不同。

`git config set user.email xxx@xxx.com` 此处邮箱需为CODE注册邮箱

`git remote add code <项目地址> ` 项目地址填写形如： `git@code.csdn.net:CSDN_Code/<项目名>.git `的SSH地址

### 2、git pull和git push

按照第一步完成设置后，一般而言，你本地代码仓将会有两个远端地址。指向github的远端主分支地址为origin master，指向CODE平台远端主分支地址为code master。

根据绑定账号时的设置，从两个平台回拉和推送代码的命令分别是：

从github回拉： `git pull origin master`  

推送到github： `git push origin master`  

从CODE回拉： `git pull code master`  

推送到CODE： `git push code master` 

为了保持本地项目处于最新状态，建议您在每次修改项目之前都是用git pull命令确认一下本地与远端的代码保持同步。   

### 3、CODE平台的自动同步功能

如果你仅将CODE平台作为github项目的镜像站，而不打算在上面做任何独立提交和更新，可以使用CODE平台的“自动同步功能”。

* 该功能只支持git版本管理项目   
* 该功能使用的是--force模式，在CODE平台上的所作改动将被清除。  
* 在CODE平台的操作不能被逆向同步到github等网站  

由于自动同步这一功能的危险性和比较占用系统资源，如果您确实需要这一功能，请**发送邮件到codesupport@csdn.net**，注明您项目的github地址和CODE地址，申请开通自动同步。