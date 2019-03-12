---
title: hexo+github最新最完整的建站过程
categories:
  - 工具
tags:
  - hexo
  - github
  - 建站
date: 2019-03-12 08:08:08
---

<a name="e204c251"></a>
# 一、注册github账号

[github注册地址](https://github.com/join)

另外github支持当前版本的Chrome、Firefox、Safari和Microsoft Edge。

填写注册信息：

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552342983814-decc6633-5fdb-41a8-9af1-c0571aaa2a90.png#align=left&display=inline&height=743&name=image.png&originHeight=928&originWidth=862&size=80387&status=done&width=690)

其中Username为你github账户的名字，取完之后就改不了了。

Email address为你的邮箱地址。

Password设置你的密码。

然后点击验证，Create an account.

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343126402-dd262640-f513-4ce3-b70a-1aedbe840adf.png#align=left&display=inline&height=686&name=image.png&originHeight=858&originWidth=835&size=92208&status=done&width=668)<br />继续Continue,<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343412568-705b5510-4611-4517-8bf4-3f1cd0b514b7.png#align=left&display=inline&height=543&name=image.png&originHeight=679&originWidth=886&size=63957&status=done&width=709)<br />这一步你可以选择跳过，也可以根据你的情况选择一下submit。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343492831-797bc009-bd60-4e1a-b96d-0663f0d24204.png#align=left&display=inline&height=284&name=image.png&originHeight=355&originWidth=768&size=43915&status=done&width=614)<br />然后确认下你的邮箱；

确认完后登录到你的github页面。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343688445-29f56ead-7174-4ed7-9aea-08ad08e5a7b3.png#align=left&display=inline&height=529&name=image.png&originHeight=661&originWidth=1907&size=130256&status=done&width=1526)<br />点击Your repositories<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343772452-c6402994-17d3-4fba-a198-df4d036987bd.png#align=left&display=inline&height=390&name=image.png&originHeight=487&originWidth=997&size=43328&status=done&width=798)

<a name="1df9ac96"></a>
# 二、创建github pages

点击New，新建一个仓库。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343884188-1adc8bf7-969f-4fd0-99a4-06edc85fd704.png#align=left&display=inline&height=463&name=image.png&originHeight=579&originWidth=779&size=56936&status=done&width=623)

Repository name必须是这种格式 `xxxx.github.io`。

xxxx为你刚刚注册github账号的名字。

点击Create repository后，跳转到下面这个页面。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552344010670-305b58c0-8c1d-4ab3-8e91-f301e8361d04.png#align=left&display=inline&height=459&name=image.png&originHeight=574&originWidth=1003&size=57563&status=done&width=802)

点击Settings 。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552344154212-99e1a683-dac3-4dbd-96d8-d0404f530051.png#align=left&display=inline&height=492&name=image.png&originHeight=614&originWidth=762&size=55288&status=done&width=610)<br />至此你的github静态页面存储库就创建成功了。不防点下你的新建的网址，`https://your_github_repostoriesName.github.io` 试试看。

<a name="e89dec64"></a>
# 三、本地连接GitHub

<a name="61b56dbf"></a>
## **生成SSH添加到GitHub**

现在我们需要在本地配置下git，让它能连接到Github仓库。

`git config --global user.name "yourname"`

`git config --global user.email "youremail"`<br /><br /><br />例如我的：

`git config --global user.name "doerteacher"`，注册github的账号名称。

`git config --global user.email "xxxxxxx@qq.com"`,注册github的邮箱。

然后创建ssh，一路回车。

**ssh-keygen -t rsa -C "youremail"**

默认生成ssh key在C:\Users\电脑用户名\ .ssh文件夹下。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552348195482-5a351223-f384-4757-9802-a9ec791b7c87.png#align=left&display=inline&height=80&name=image.png&originHeight=100&originWidth=320&size=4356&status=done&width=256)

然后在GitHub的setting中，找到SSH keys的设置选项，点击`New SSH key`把你id_rsa.pub里面的信息复制进去。

点击Setting，进入SSH and GPG keys页面。<br />
![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552348293842-40f2c8b7-669d-48a9-a7c6-b0ad8f1d8009.png#align=left&display=inline&height=544&name=image.png&originHeight=680&originWidth=1575&size=107304&status=done&width=1260)<br />点击SSH and GPG keys，然后点击New SSH key。<br />
![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552348350591-c9bc23fe-13c8-47ae-820e-f7692ece0c69.png#align=left&display=inline&height=481&name=image.png&originHeight=601&originWidth=1077&size=50769&status=done&width=862)<br />Title随便起个名，比如blog。把id_rsa.pub里面的信息复制到Key里面。<br />
![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552348382771-e47ae0ce-2eeb-468d-9d29-56bed3a0c01c.png#align=left&display=inline&height=459&name=image.png&originHeight=574&originWidth=1106&size=43953&status=done&width=885)

然后输入

**ssh -T git@github.com**

检测下是否配置成功。

然后会得到如下信息，证明你配置成功了。<br /><br />Hi DoerTeacher! You've successfully authenticated, but GitHub does not provide shell access. 


<a name="95a104f2"></a>
# 四、Hexo创建

<a name="f3b79a1d"></a>
## Hexo创建前环境准备

<a name="e4f8a1ca"></a>
### Git安装

[下载Git](https://git-scm.com/downloads)

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552344804893-25d65ea4-ec7f-4bd4-8e27-ae6e2c05d17d.png#align=left&display=inline&height=496&name=image.png&originHeight=620&originWidth=668&size=116395&status=done&width=534)

基于你电脑的系统自行选择下载哪个版本。

如果不会Git怎么安装的话，网上自己搜索下Git具体安装步骤。

<a name="abaa35be"></a>
### nodejs安装

[nodejs下载](https://nodejs.org/zh-cn/download/)

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552345110497-7134da09-06a1-47ad-89b6-98c2dff03301.png#align=left&display=inline&height=555&name=image.png&originHeight=694&originWidth=1267&size=128873&status=done&width=1014)

基于你电脑的系统自行选择下载哪个版本。


如果不会nodejs怎么安装的话，网上自己搜索下Git具体安装步骤。


安装完后，打开cmd工具,输入`node -v` 检测下安装的版本。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552345398313-13b77c10-5438-4dd4-8b13-9a2ef4831201.png#align=left&display=inline&height=89&name=image.png&originHeight=111&originWidth=591&size=7537&status=done&width=473)

至此nodejs安装完毕。

接下来就可以真正安装hexo了。

<a name="fbe3b6b3"></a>
## Hexo安装

首先在自己电脑的D盘，建个存储Hexo文件的文件夹。

例如我在D盘user文件夹下新建了个Hexo文件夹：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552345908358-a37420e3-9682-4612-bd3a-5e554d102952.png#align=left&display=inline&height=103&name=image.png&originHeight=128&originWidth=327&size=4484&status=done&width=262)
<a name="d41d8cd9"></a>
## 
然后打开自己电脑的Git Bash

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346031892-0997d4c2-c2a5-43a3-a7bf-ce4579b0fe81.png#align=left&display=inline&height=78&name=image.png&originHeight=98&originWidth=118&size=12274&status=done&width=94)


然后cd到Hexo文件夹下，输入 `npm install -g hexo-cli`，安装hexo。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346176052-0a17db11-f194-4df0-bcfa-f6cd368aac22.png#align=left&display=inline&height=359&name=image.png&originHeight=449&originWidth=745&size=26094&status=done&width=596)

输入`hexo -v`，看下hexo当前版本

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346440128-eb6e89a3-d948-4385-a845-ad8f1bd25da7.png#align=left&display=inline&height=253&name=image.png&originHeight=316&originWidth=562&size=23636&status=done&width=450)

然后初始化hexo

`hexo init blog`

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346588851-ef64b589-3fbf-497a-b229-0227e09bf248.png#align=left&display=inline&height=259&name=image.png&originHeight=324&originWidth=604&size=51696&status=done&width=483)

然后cd到刚刚初始化的blog文件夹下。<br />`cd blog/`<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346715431-3a546a4d-2cef-45b5-81dc-aae4c867a60d.png#align=left&display=inline&height=107&name=image.png&originHeight=134&originWidth=566&size=15309&status=done&width=453)

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346642493-c800511e-3057-498c-8ab5-9bfa686eed3e.png#align=left&display=inline&height=248&name=image.png&originHeight=310&originWidth=344&size=16644&status=done&width=275)

这时你会发现新建了这么几个文件。

然后安装npm 依赖项。

`npm install`

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346838820-534ee804-7a45-4eb4-b26c-cc5c2ab4cfc5.png#align=left&display=inline&height=159&name=image.png&originHeight=199&originWidth=736&size=26801&status=done&width=589)

然后`hexo g`，生成静态文件。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552346971701-78ce54f9-f446-486c-8e87-d893285c2ec2.png#align=left&display=inline&height=170&name=image.png&originHeight=212&originWidth=531&size=27308&status=done&width=425)


然后 `ls`,你会发现多了`public`文件夹，这就是生成的静态文件页面。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552347015283-9a8a60dd-7f6c-4f27-b4dd-3871d2413364.png#align=left&display=inline&height=76&name=image.png&originHeight=95&originWidth=639&size=11345&status=done&width=511)

然后hexo server 启动服务器。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552347108693-bbbaf94d-41a4-4201-be5a-cd8ebb1369cf.png#align=left&display=inline&height=76&name=image.png&originHeight=95&originWidth=676&size=10764&status=done&width=541)

访问网址为： http://localhost:4000/

![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552347171072-af25c97e-fe4f-44c3-be02-cb47c1b0e1d6.png#align=left&display=inline&height=778&name=image.png&originHeight=973&originWidth=1354&size=343524&status=done&width=1083)

然后就进入了hello world的页面。

这时就代表了你的hexo安装完成了。

前面我们已经在github上建了存储静态页面的仓库并配置了本地连接Github。

然后我们就可以把hexo生成的页面部署到github上了。

<a name="ce7c9c65"></a>
# 五、**将hexo部署到GitHub**

打开站点配置文件 `_config.yml`，在刚才生成的blog目录下。<br /><br /><br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552349295804-1380d08e-58dd-4481-96e2-772e3d56bfd4.png#align=left&display=inline&height=228&name=image.png&originHeight=285&originWidth=349&size=15724&status=done&width=279)<br /><br /><br />在_config.yml最下面，找到deploy：


![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552349418958-e4538a71-9b03-4145-ac1b-260d1d88d35b.png#align=left&display=inline&height=704&name=image.png&originHeight=880&originWidth=1092&size=86598&status=done&width=874)<br />修改为<br /><br /><br />

	deploy:                                                                                                                                                               
		type: git                                                                                                                                                        
		repository: git@github.com:DoerTeacher/doerteacher.github.io.git 
		branch: master


DoerTeacher就是我的GitHub账户名，你得改成你自己的。

repository地址也可以到自己GitHub账户的仓库下复制。


![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552349934196-9e3c5ea9-b9f5-40ba-b87a-01af2988f52f.png#align=left&display=inline&height=524&name=image.png&originHeight=655&originWidth=1018&size=77292&status=done&width=814)

然后安装 部署到github插件的依赖<br /><br /><br />**`npm install hexo-deployer-git --save`**<br /><br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552350137456-e839299a-1014-422a-8ba6-721987b0b97c.png#align=left&display=inline&height=196&name=image.png&originHeight=245&originWidth=707&size=36508&status=done&width=566)<br /><br /><br />这个时候就可以开始真正地讲hexo部署到github上了。<br /><br /><br />**hexo deploy**
<br /><br /><br />然后就可以在`http://doerteacher.github.io` ，访问你自己的博客了。


其中`doerteacher.github.io`为你之前创建的Repository Name。<br />![](https://cdn.nlark.com/yuque/0/2019/png/286890/1552343884188-1adc8bf7-969f-4fd0-99a4-06edc85fd704.png#align=left&display=inline&height=554&originHeight=579&originWidth=779&status=done&width=746)

然后你就可以看到这样的页面了。


![image.png](https://cdn.nlark.com/yuque/0/2019/png/286890/1552350719207-e400f3de-9ab8-4675-b7a2-4cdc1cab028b.png#align=left&display=inline&height=747&name=image.png&originHeight=934&originWidth=1920&size=438949&status=done&width=1536)

至于hexo的使用、添加评论功能、绑定自定义域名，以及自动化集成部署我将会在下一篇博文中完整地整理出来。
