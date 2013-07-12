## 我有一个项目，我想托管在CODE上


**在此操作之前需要您[配置本地git环境](/help/CSDN_Code/code_support/FAQ_2_2)。**

然后判断您想上传的项目是否是一个git版本管理的项目。

### 不是git版本管理项目的情况：

#### 1、新建项目

在CODE平台上新建一个项目，项目名最好不要与你原来的项目重名（避免将此项目下载下来的时候出现命名冲突），创建项目时切记勾选“使用README.md文件初始化”

* [如何创建新项目？](/help/CSDN_Code/code_support/FAQ_2_1)  


#### 2、下载项目

在git命令行界面输入git clone+项目地址，将刚刚创建的项目下载下来。
形如：

    git clone git@code.csdn.net:xxx/xxx.git  

#### 3、复制原有项目代码到git项目

把原有项目的所有代码复制到刚刚下载的git项目文件夹里

#### 4、上传项目

将添加了文件的项目push到CODE平台上 

使用如下命令将项目上传到CODE平台

    $ 进入此项目所在文件夹  
    $ git init  
    $ git add .  
    $ git commit -m “first commit”  
    $ git remote add origin <项目url, 如git@code.csdn.net:xxx/xxx.git>  
    $ git push -u origin master   


---

### 是git版本管理项目的情况：

#### 1、新建项目

在CODE上创建一个项目，名称与原项目相同，记得**去除“使用README.md文件初始化”选项前面的对勾**

![](/images/new_2_1.jpg)

#### 2、上传本地项目

使用如下命令将项目上传到CODE平台

    $ 进入此项目所在文件夹  
    $ git init  
    $ git add .  
    $ git commit -m “first commit”  
    $ git remote add origin <项目url, 如git@code.csdn.net:xxx/xxx.git>  
    $ git push -u origin master   
