## 已有一个项目，想托管在CODE上


**在此操作之前需要您[配置本地git环境](/help/CSDN_Code/code_support/FAQ_2_2)。**

然后判断您想上传的项目是否是一个git版本管理的项目。

### 不是git版本管理项目的情况：

#### 1、新建项目

在CODE上创建一个项目，名称与原项目相同，记得**去除“使用README.md文件初始化”选项前面的对勾**

![](/images/new_2_1.jpg)

* [如何创建新项目？](/help/CSDN_Code/code_support/FAQ_2_1)  

#### 2、上传项目

使用如下命令将项目push到CODE平台

    $ cd <项目所在文件夹>  
    $ git init  
    $ git add .  
    $ git commit -m “first commit”  
    $ git remote add origin <项目url, 如git@code.csdn.net:xxx/xxx.git>  
    $ git push -u origin master   


---

### 已经是git版本管理项目的情况：

#### 1、新建项目

在CODE上创建一个项目，名称与原项目相同，同样记得不要**使用README.md文件初始化**

#### 2、上传本地项目

使用如下命令添加CODE成新远端，并将项目上传到CODE平台

    $ cd <项目所在文件夹>  
    //添加新远端，名称为code
    $ git remote add code <项目url, 如git@code.csdn.net:xxx/xxx.git>  
    //上传代码
    $ git push -u code master