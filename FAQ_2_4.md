##上传本地项目

**没有使用Readme文件初始化的项目**

使用此选项创建的项目，多数情况是用户已经在本地有了一个项目。想把此项目变成使用Git管理。

	进入此项目所在文件夹
	git init
	git add .
	git commit -m “first commit”
	git remote add origin <项目ssh url, git@code.csdn.net:xxx/xxx.git>
	git push -u origin master
    
**使用Readme文件初始化的项目**
使用此选项创建的项目，用户需要首先在本地将网站上的项目Clone下来，才能进一步进行文件上传。

	git clone <项目ssh url, git@code.csdn.net:xxx/xxx.git>
	做些更新
	git push