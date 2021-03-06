# 前言

　　各位 HR，面试官你们好，欢迎来到我的 Github。为了能更好的介绍自己的项目，特别创建本仓库介绍我的项目，顺便也是对自己过去的项目回顾和总结。

　　在这里我将描述项目背景、项目简介、技术栈、我的工作、难点、遇到的困难、优化。



# 项目目录

1. 在线存证平台
2. 信息化考勤
3. 影像管理系统
4. 宫颈细胞筛查分类
5. 学代会换届选举投票系统
6. 华东计算机基础研究会官网



说明：在这里我将详细介绍 `1-3` 的项目说明，`4-6` 则会简单描述。



# 项目说明

## 1. 在线存证平台

### 1.1 项目时间

2018/3 - 2018/5

### 1.2 项目简介

- 第三方电子证据综合服务平台，通过在线签署借款电子合同，保证签署双方的身份主体信息真实有效。借款人和投资人通过平台签署借款协议，使得借款流程有理有据，保证了双方的合法权益，减少双方的不必要纠纷。
- 实现小程序客户端、Web后台管理的在线借据存证平台

### 1.3 技术实现

- Java Web 框架：SpringBoot
- 数据库：MySQL 5.6 + Redis
- 服务器：Centos 7.3
- 移动端实现：微信小程序
- 系统后台管理：vue.js + bootstrap
- 文档技术：接口文档使用 apidoc，项目说明使用 kancloud 在线文档
- 代码托管：码云

### 1.4 我的工作

- 需求分析，前后台技术选型
- 数据库设计、定时备份、Redis缓存
- Java 后台 RESTful API 接口开发（实现 JWT 接口验证）
- HTTPS 证书配置、Nginx 代理
- Linux 正式、测试服务器搭建
- 对接第三方接口平台（包括：微信支付、银行卡四要素验证、短信服务）
- 后台实现定时任务、短信消息队列
- 业务逻辑、流程图

### 1.5 项目难点

- 暂时还没想好

### 1.6 项目优化

- 待完善

### 1.7 项目代码

```powershell
PS D:\dev> .\cloc-1.76.exe .\mango_server\
github.com/AlDanial/cloc v 1.76  T=1.00 s (297.0 files/s, 31021.0 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JavaScript                      66            370            790           6539
Java                            90           1620           2633           6331
XML                            120              0              0           5078
JSON                             5              3              0           4787
SQL                              1             20             57            787
HTML                             2             63              0            607
CSS                              4             98             37            492
Bourne Shell                     1             29             51            145
DOS Batch                        2             32              0            114
Maven                            1             36             53            110
Markdown                         3             16              0             64
YAML                             2              8              0             51
-------------------------------------------------------------------------------
SUM:                           297           2295           3621          25105
-------------------------------------------------------------------------------
```

### 1.8 项目展示

接口文档（使用 `apidoc` 工具编写）

- [RESTful API在线文档](https://api.chengchijinfu.com/mango/apidoc/index.html)



小程序移动端入口（二维码）

<div align="left"><img src="assets/5b32e5171c1ad.jpg" width="250"/></div>



移动端截图

<div align="left"><img src="assets/mango_wx.jpg" width=""/></div>



系统后台截图

<div align="left"><img src="assets/mango1.png" width=""/></div>

<div align="left"><img src="assets/mango2.png" width=""/></div>

<div align="left"><img src="assets/mango3.png" width=""/></div>

<div align="left"><img src="assets/mango4.png" width=""/></div>



## 2. 考勤在线

### 2.1 项目时间

2017/3 - 2017.7

### 2.2 项目简介

现如今企业内部信息平台诸多，但平台的关联性较小。本系统将通过信息化技术，实现信息联通，打通数据孤岛，解决内部多平台、多站点、多数据库的现状。以移动微信企业号为移动终端，Web考勤在线为 PC 终端，实现企业社区、考勤管理、工单管理、财务管理等等功能模块。

当前已经完善的主要是考勤在线模块。

自 2017年7月 以来，系统已正常运行一年时间，不间断维护和升级。

### 2.3 技术实现

- 移动端实现：微信企业号

- 系统后台管理：vue.js + ElementUI

- 服务端语言：PHP（Thinkphp） + Java（SSM）
- 数据库
  - 内网数据库：SqlServer
  - 平台数据库：MySQL
- NoSQL：Redis
- 服务器：
  - 门禁考勤服务器：Windows Server 2008
  - 平台服务器：Centos 6.4
- 文档技术：接口文档使用 apidoc，项目说明使用 miniDoc （自行搭建的文档平台）
- 代码托管：自行搭建的 VisualSVN 服务

### 2.4 我的工作

- 需求分析
- 数据库设计
- 服务器环境搭建
- 不同数据库 ETL 仓库同步

- HTTPS 证书配置
- 后台 RESTful API 接口文档开发 | [点击查看接口文档](http://user.renrunkeji.com/apidoc/)
- 消息接口中心实现（信息平台最重要的是消息送达服务，在这里实现了如下的消息通知机制）
  - 微信企业号图文、文本、模板消息推送机制
  - 短信消息推送
  - 邮件消息推送
  - 企业内部旧办公 OA 消息推送

### 2.5 项目难点

- 内网 SqlServer 与 MySQL 数据仓库 ETL 实时同步
- 业务流程参数化配置
- 附件上传管理，图片压缩

### 2.6 项目优化

- 消息 Socket 通知

### 2.7 项目代码

```powershell
T=5.00 s (132.8 files/s, 51105.0 lines/s)
-------------------------------------------------------------------------------
Language                     files          blank        comment           code
-------------------------------------------------------------------------------
JavaScript                     232           4400           7204         142678
PHP                            346           6561          23519          55239
CSS                             13            354             91           7611
JSON                            43             12              0           4136
HTML                             9            179             17           2048
MSBuild script                   1              0              0            520
YAML                             5             70             34            193
C                                2             31             33            183
Smarty                           3              0              0            174
Markdown                         6             44              0             87
C/C++ Header                     2             29             26             41
m4                               1              1              0              6
INI                              1              0              0              4
-------------------------------------------------------------------------------
SUM:                           664          11681          30924         212920
-------------------------------------------------------------------------------
```

### 

### 2.8 项目展示









## 3. 影像管理系统

### 3.1 项目时间

2017/3 - 2017.7

### 3.2 项目简介



### 3.3 技术实现



### 3.4 我的工作



### 3.5 项目难点



### 3.6 项目优化



### 3.7 项目代码



### 3.8 项目展示





2017.10-2017.12

以杭州锦江集团财务审批为背景，实现桌面应用端和Web端，扫描仪扫描图片，图片条形码识别，影像上传管理系统。文件系统基于OpenCMIS，并实现Web第三方RESTful Api接口。【个人项目】

基于OpenCMIS实现了Web端第三方API接口





## 4. 宫颈细胞筛查分类

2017.10-2017.12

医疗辅助诊断系统。对宫颈细胞显微镜下图片分割，特征提取。对宫颈鳞状单细胞，基于特征，应用机器学习算法进行分类。【实验室项目】





## 5. 学代会换届选举投票系统

### 5.1 项目时间

2015-2017

### 5.2 项目简介

同时在学生工作之余，也为学代会换届投票选举开发了在线实时投票系统，高效解决选票计票的繁琐问题。并实践了三年的版本迭代

地址：http://hise.frankfeekr.top/hise/admin

![](assets/hise_vote_wx.jpg)

![](assets/hise_vote_chart.png)





## 6. 华东计算机基础研究会官网

### 6.1 项目时间

2015/4

### 6.2 项目简介

主要是一个新闻管理、图片管理的网站。

在校期间，刚接触web网站编程的那段时间，实现了一个新闻网站的全站点开发。主要应用的是 ASP.NET 进行开发的，回过头来看如今前后端分离的开发模式，现在已经完全都抛弃了这种开发方式。 

这里就不详细描述了，直接上官网地址吧：http://cai.hznu.edu.cn/hdgx/





# 后记

这里是后记说明

▶