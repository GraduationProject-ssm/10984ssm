# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10984ssm留学生交流互动论坛网站

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=82)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

留学生交流互动论坛网站工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。留学生交流互动论坛网站的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示学生工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、学生信息实体图如图4-3所示：

![](/md/blog.014.png)

`   `图4-3学生信息实体图

2、计划分享信息实体图如图4-4所示：

![](/md/blog.015.png)

`       `图4-4计划分享信息实体图

3、经验分享信息实体图如图4-5所示：

![](/md/blog.016.png)

`       `图4-5经验分享信息实体图
#########
4、网址推荐信息实体图如图4-6所示：

![](/md/blog.017.png)

`        `图4-6网址推荐信息实体图

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表1：jihuafenxiang表

|列名|数据类型|长度|约束|
| - | - | - | - |
|id|bigint|19|NOT NULL|
|addtime|varchar|2000|` `NULL DEFAULT |
|jihuamingcheng|tinyint|2|` `NULL DEFAULT |
|zhanghao|varchar|2000|` `NULL DEFAULT |
|xingming|varchar|2000|` `NULL DEFAULT |
|zhaopian|varchar|2000|` `NULL DEFAULT |
|fangfaneirong|varchar|2000|` `NULL DEFAULT |
|fangfaxiangqing|varchar|2000|` `NULL DEFAULT |
|qitajianyi|varchar|2000|` `NULL DEFAULT |
|fabushijian|varchar|2000|` `NULL DEFAULT |
|fengmiantupian|varchar|2000|` `NULL DEFAULT |

表2：jingyanfenxiang表

|列名|数据类型|长度|约束|
| - | - | - | - |
|id|bigint|19|NOT NULL|
|addtime|varchar|2000|` `NULL DEFAULT |
|biaoti|tinyint|2|` `NULL DEFAULT |
|zhanghao|varchar|2000|` `NULL DEFAULT |
|xingming|varchar|2000|` `NULL DEFAULT |
|biaoqian|varchar|2000|` `NULL DEFAULT |
|neirong|varchar|2000|` `NULL DEFAULT |
|gerenxiangfa|varchar|2000|` `NULL DEFAULT |
|zhaopian|varchar|2000|` `NULL DEFAULT |
|shipinfenxiang|varchar|2000|` `NULL DEFAULT |
|fabushijian|varchar|2000|` `NULL DEFAULT |
|fengmiantupian|varchar|2000|` `NULL DEFAULT |

表3：ruanjiantuijian表

|列名|数据类型|长度|约束|
| - | - | - | - |
|id|int|11|NOT NULL|
|addtime|varchar|255|NOT NULL|
|ruanjianmingcheng|varchar|255|NOT NULL|
|ruanjianjieshao|varchar|2|NOT NULL|
|zhanghao|varchar|2|NOT NULL|
|xingming|varchar|2|NOT NULL|
|zhaopian|varchar|2|NOT NULL|
|ruanjianlaiyuan|varchar|2|NOT NULL|
|shipinfenxiang|varchar|2|NOT NULL|
|fabushijian|varchar|2|NOT NULL|
|ruanjianxiangqing|varchar|2|NOT NULL|
|fengmiantupian|varchar|2|NOT NULL|

表4：xuesheng表

|列名|数据类型|长度|约束|
| - | - | - | - |
|id|` `int|9|NOT NULL |
|addtime|char|5|NOT NULL|
|zhanghao|char|5|NOT NULL|
|mima|char|5|NOT NULL|
|xingming|char|5|NOT NULL|
|xingbie|char|5|NOT NULL|
|nianling|char|5|NOT NULL|
|shouji|char|5|NOT NULL|
|youxiang|char|5|NOT NULL|
|shenfenzheng|char|5|NOT NULL|
|zhaopian|char|5|NOT NULL|

#########
# 5系统界面实现
## 5.1 管理员登录
管理员输入个人的用户名、密码和角色登录系统，这时候系统的数据库就会在进行查找相关的信息，如果我们输入的用户名、密码和角色不正确，数据库就会提示出错误的信息提示，同时会提示管理员重新输入自己的用户名、密码、角色，直到账号密码输入成功后，会提登录成功的信息。网站管理员登录效果图如图5-1所示：

![](/md/blog.018.png)     
图5-1管理员登录界面

## 5.2  管理员功能模块     
### 5.2.1 学生管理
管理员对学生管理进行编辑查看账号、姓名、性别、年龄、手机、邮箱、身份证、照片并进行详情、删除、修改等操作。程序成效图如下图5-2所示:

![](/md/blog.019.png)

图5-2学生管理界面图
### 5.2.2 经验分享管理
管理员对经验分享管理进行查看标题、账号、姓名、标签、内容、照片、视频分享、发布时间、封面图片等信息并可以进行详情、删除、修改操作。程序效果图如下图5-3所示：

![](/md/blog.020.png)

图5-3经验分享管理界面
### 5.2.3 计划分享管理
管理员对计划分享管理进行查看计划名称、账号、姓名、照片、方法内容、其他建议、发布时间、封面图片等信息并可以进行详情、删除、修改操作。程序效果图如下图5-4所示：

![](/md/blog.021.png) 

图5-4计划分享管理界面

### 5.2.4网址推荐管理
管理员对网址推荐管理进行查看网址名称、网址介绍、姓名、账号、照片、网址来源、视频分享、发布时间、封面图片等信息进行详情、删除、修改操作。程序效果图如下图5-5所示：

![](/md/blog.022.png)

图5-5网址推荐管理界面
### 5.2.5留言板管理
管理员对留言板管理进行查看用户名、留言内容、回复内容等信息并可以进行详情、删除、修改操作。程序效果图如下图5-6所示：

![](/md/blog.023.png) 

图5-6留言板管理界面
## 5.3 前台首页功能模块
前台首页详情页面：首页、经验分享、计划分享、软件推荐、网址推荐、交流论坛、学习资讯、留言反馈、个人中心、后台管理等功能操作。程序效果图如下图5-7所示：

![](/md/blog.024.png)

图5-7前台首页功能界面
## 5.3.1 学生登录、学生注册
学生在线填写账号、密码、姓名、性别、年龄、手机、邮箱、身份证等信息进行注册、登录操作。程序效果图如下图5-8所示：

![](/md/blog.025.png)

![](/md/blog.026.png)

图5-8学生登录、学生注册界面
## 5.3.2经验分享
学生进入经验分享可以查看标题、账号、姓名、标签、内容、照片、视频分享、发布时间、封面图片等信息，并可以进行提交操作。程序效果图如下图5-9所示：

![](/md/blog.027.png)


图5-9经验分享界面
## 5.3.3个人中心
学生进入个人中心可以查看账号、姓名、性别、年龄、手机、邮箱、身份证、照片进行更新信息、退出登录操作。程序效果图如下图5-10所示：

![](/md/blog.028.png)

图5-10个人中心界面

## 5.4 学生功能模块

## 5.4.1经验分享管理
学生进入经验分享管理可以查看标题、账号、姓名、标签、内容、照片、视频分享、发布时间、封面图片等信息进行详情、修改、删除操作。程序效果图如下图5-11所示：

![](/md/blog.029.png)

图5-11经验分享管理界面
## 5.4.2计划分享管理
学生进入计划分享管理可以查看计划名称、账号、姓名、照片、方法内容、其他建议、发布时间、封面图片并可以进行详情、删除等操作。程序效果图如下图5-12所示：

![](/md/blog.030.png)

图5-12计划分享管理界面

## 5.4.3网址推荐管理
学生进入网址推荐管理可以查看网址名称、网址介绍、姓名、账号、照片、网址来源、视频分享、发布时间、封面图片并可以进行详情、删除等操作。程序效果图如下图5-13所示：

![](/md/blog.031.png)

图5-13网址推荐管理界面














