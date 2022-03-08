# sentry

Sentry系统结合大华旗下监控摄像头，实现监控范围内的多个人脸同时进行 检测、跟踪，并与百度云人脸数据库进行实时比对，实现快速身份识别，可提供24小时监控、数据分析和人脸库管理。
## Sentry项目介绍

**项目背景**

由目前对于来访人员管理还处于人工管理或人工+监控，具有安全隐患和资源浪费并且单一的实时监控不能满足现代人们对于安全保障方面的需要，所以Sentry系统在监控的基础上加上了数据分析，以及人脸识别，可以针对不同时段的不同操作产生可视化报表，方便安保人员随时查看分析出想要的信息。结合上人脸识别的监控设备，Sentry还提供人脸库管理功能，不需要任何其他存储设备，直接在可视化界面上对人脸照进行添加、修改、删除、查看的一键式操作。

**面向群体**

公司、学校、单位等对进出人员严格控制的场所。 

**核心思想**

无人化：
前台、大门不需要时时有人看管，Sentry系统会24小时监控并报警，并把陌生人的人脸照截取下来，保留识别到陌生人的数据，时间精确到秒。
易使用：
无需培训即可快速上手，多为可视化界面，操作简便，下载安装即用。系统设置掉线自动登录，只要保证联网系统即可运行。

**产品亮点**
1.性能高效、系统可靠 识别准确度高、速度快，结合百度智能云人脸库，即时报警 多人脸实时监测：能同时检测和识别同一监控视频中的多个人脸 2.管理简单、操作灵活 界面友好：图形化监控管理，可视化人脸库管理
兼容性强：适用于多种大华型号监控设备
集中管理：采用分布式架构，对多路摄像头进行集中管理
3.数据持久化、快速分析 数据保留：每次识别的产生的数据（成功/失败、时间、人脸照等）都会存入数据库，方便后期进行查看、分析。
报表分析：针对不同时段的不同操作产生可视化报表，可根据不同种类的报表分析需要的信息。

**产品框架**
Winfrom  WCF 

**实际展示（截图或视频）**

一、主界面
监控壹佰八楼23个摄像头的分布平面图。
![在这里插入图片描述](https://img-blog.csdnimg.cn/9f08b38b66b44574b39a984270534b43.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)


 
鼠标移到任意摄像头的位置，展示该摄像头画面，光标移动到摄像画面再移开则关闭摄像画面。
![在这里插入图片描述](https://img-blog.csdnimg.cn/514c8c9aa6f94f65854cb8ae50b9523f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
当有陌生人经过时提示、发出报警声。
![在这里插入图片描述](https://img-blog.csdnimg.cn/291667f1799640db8b445bf40b49b48f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
按Esc或空格键关闭报警，弹出人脸添加窗体。
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/554d9300ef69432c9bba3a893201bf62.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_10,color_FFFFFF,t_70,g_se,x_16)
二、人脸库管理
点击主页面的 按钮，可显示人脸库管理页面。
功能：可以按姓名查询照片、修改照片信息、删除照片。
![在这里插入图片描述](https://img-blog.csdnimg.cn/354525ab3c9e47669e8fa4eab994bd18.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
（1）通过姓名查询照片
![在这里插入图片描述](https://img-blog.csdnimg.cn/a237adfe443b4d85a80d260ebc86ae41.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/192fec0800024f6ca84c848dff9fa361.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16) 
 
（2）修改、删除照片操作
鼠标右击照片弹出照片信息（用户姓名与用户性别），可进行修改或删除操作。
![在这里插入图片描述](https://img-blog.csdnimg.cn/8208713e87f449b181ff8602f383c0c3.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_10,color_FFFFFF,t_70,g_se,x_16)

（3）人脸库管理页面点击  按钮 添加照片窗体。
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/2e3fb78769a040e6a3d0bbeed661634f.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_11,color_FFFFFF,t_70,g_se,x_16)

三、数据分析
主页面右上角的 ![在这里插入图片描述](https://img-blog.csdnimg.cn/d3ab794ede004134b12b42c8e867097d.png)（数据分析按钮），可以生成三种类型的报表，可以按钮日、周、月不同的时间划分查看数据。可以按需要随意切换柱状图、折线图和饼状图。 
![在这里插入图片描述](https://img-blog.csdnimg.cn/16ea27a9c145435593b133c891f805ec.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)

## 应用场景 

### 介绍
哨兵系统主要应用于楼层的安全监控，自动化进行全天候监视提醒，这个过程不需要进行手动操作，只有对报警信息进行处理即可。适用于公司写字楼和学校教学楼等 
### 时间
哨兵系统默认全天候24h运行，只要监控系统硬件是打开状态，哨兵系统就一直运行 
### 地点
哨兵系统分为终端和服务器，终端分为每个房间部署的摄像头，和前台的监视器以及收音设备。后端部署在公司的服务器上。 人物 楼层熟人(工作人员，学生等)、访客、值班人员(管理员)
### 行为
进行人脸库的添加、修改、删除、信息更新
![在这里插入图片描述](https://img-blog.csdnimg.cn/8c7daace363e43ad832810a9e40f7842.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)

进行监控的实时查看   
![在这里插入图片描述](https://img-blog.csdnimg.cn/5a66fc3dd31d46979794e406a54f7912.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)

处理访客信息提醒和陌生人报警  
![在这里插入图片描述](https://img-blog.csdnimg.cn/40c99258a1114ad297ab31dffa08ecec.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)

 ## 项目部署文档：
 部署环境：windows下的iis服务
 一、打开iis服务
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/d19be9be7aee4dd992178eb5f2513df2.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
 二、在网站目录中新建网站，并将后端代码部署到新建的网站下  
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/0d7368834e084db0b87499bee9c8b190.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
 三、编辑权限：将文件夹安全属性中添加everyone的权限配置  
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/e31ae24aa3e744daabd0716cc93f4293.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
 四、点击画圈页面
  ![在这里插入图片描述](https://img-blog.csdnimg.cn/015c852a06ae4f738404155475f88b74.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
  
 出以下界面表示部署成功了
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/7455b80c9d3d41cd80f5116782bff460.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)

![在这里插入图片描述](https://img-blog.csdnimg.cn/cd63b06d687b427ba8fb0b5340de62ed.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
 ### 五、前端调用
 添加引用：使用visual  studio打开项目  FaceRecognition的Connected Services  添加服务引用
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/9d844a5da0f24c07a3b0000453ffe9f9.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBA546L5Y2r4oCU4oCURGF2aWQ=,size_20,color_FFFFFF,t_70,g_se,x_16)
 
 地址输入自己上一步的IP地址，调用后端地址就可以了
 
### 六、数据库配置
人脸识别记录表
CREATE TABLE `t_face_recognition_record`  (
  `id` int(15) NOT NULL AUTO_INCREMENT COMMENT '自增长id',
  `face_recognition` int(1) NOT NULL COMMENT '人脸识别：0失败，1成功',
  `face_photos` blob NULL COMMENT '人脸照片',
  `face_name` varchar(5) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '识别出来的人的信息',
  `create_time` datetime NOT NULL COMMENT '创建日期',
  `update_time` datetime NULL DEFAULT NULL COMMENT '更新日期',
  `is_delete` int(1) NOT NULL COMMENT '0未删除，1已删除',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB AUTO_INCREMENT = 2975 CHARACTER SET = utf8 COLLATE = utf8_general_ci COMMENT = '人脸识别记录表' ROW_FORMAT = Compact;
补充人脸记录表
CREATE TABLE `t_upload_face_database_records`  (
  `id` int(15) NOT NULL AUTO_INCREMENT COMMENT '自增id',
  `face_photos` blob NOT NULL COMMENT '人脸照片',
  `face_name` varchar(5) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '人脸姓名',
  `remarks` varchar(255) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '其他信息（备注）',
  `create_time` datetime NOT NULL COMMENT '上传时间',
  `update_time` datetime NULL DEFAULT NULL COMMENT '更新时间',
  `is_delete` int(1) NOT NULL COMMENT '0没删除，1已删除',
  PRIMARY KEY (`id`) USING BTREE
) ENGINE = InnoDB AUTO_INCREMENT = 24 CHARACTER SET = utf8 COLLATE = utf8_general_ci COMMENT = '补充人脸记录' ROW_FORMAT = Compact;

人脸信息表
CREATE TABLE `t_faceimage_info`  (
  `user_ID` varchar(20) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '用户id',
  `image_Byte` longblob NOT NULL COMMENT '图片格式',
  `face_Token` varchar(100) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '百度人脸列表',
  `is_Delet` varchar(4) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '是否删除',
  `user_Name` varchar(20) CHARACTER SET utf8 COLLATE utf8_general_ci NOT NULL COMMENT '用户名',
  `sex` varchar(2) CHARACTER SET utf8 COLLATE utf8_general_ci NULL DEFAULT NULL COMMENT '性别',
  `create_Time` datetime NULL DEFAULT NULL COMMENT '创建时间',
  `update_Time` datetime NULL DEFAULT NULL COMMENT '更新时间',
  PRIMARY KEY (`face_Token`, `user_Name`) USING BTREE
) ENGINE = InnoDB CHARACTER SET = utf8 COLLATE = utf8_general_ci COMMENT = '人脸信息' ROW_FORMAT = Compact;

## 建议新功能

### 钉钉卡片消息通知

进行人脸识别之后如果识别的人为陌生人则在弹出报警弹窗的同时，给相应负责人发送可点击按钮钉钉卡片，将陌生人人脸图片附在钉钉卡片上，点击钉钉卡片按钮处理，如果未能及时处理，卡片显示已失效。
发送钉钉卡片接口
[发送钉钉互动卡片接口](https://open.dingtalk.com/document/robots/send-interactive-dynamic-cards)

这里要说明一下，本系统使用的钉钉卡片实现的用户互动，所以需要回调， 

[钉钉互动卡片回调地址注册接口](https://open.dingtalk.com/document/robots/register-an-interaction-card-callback-address)

[更新钉钉互动卡片接口文档](https://open.dingtalk.com/document/robots/update-dingtalk-interactive-cards)

[钉钉卡片搭建平台](https://open.dingtalk.com/document/resourcedownload/card-building-platform)

可以在互动卡片搭建平台设计业务需要的钉钉卡片。
 ![在这里插入图片描述](https://img-blog.csdnimg.cn/3c570a7d008c41c48f3825410e8b2567.png)

### 语音交互功能

提供与访客进行智能语音交互的功能，实现无人化管理。当进行人脸识别之后根据人脸识别的结果采取不同的语音交互策略。
	可以采用讯飞提供的语音识别服务，进行语音听写。

[讯飞语音听写](https://www.xfyun.cn/services/voicedictation)

### 访客问卷+语音通信
由于目前新冠疫情的原因，很多场所是通过扫描二维码的形式进行信息记录。完全可以借鉴到我们的系统中来。访客来访问卷，用户通过微信扫描二维码，填写用户信息以及访问缘由当访客提交问卷的同时给被访问人拨打电话。
[阿里云语音服务](https://help.aliyun.com/document_detail/148280.html)

参考博客：[阿里云 语音服务-国内语音服务](https://blog.csdn.net/wangwei021933/article/details/123010171?spm=1001.2014.3001.5501)



## 贡献者契约行为准则

### 我们的誓言
为了营造一个开放、友好的环境，我们作为贡献者和维护人承诺，让我们的社区和参 与者，拥有一个无骚扰的体验，无论年龄、体型、残疾、种族、性别特征、性别认同 和表达、经验水平、教育程度、社会状况，经济地位、国籍、个人外貌、种族、宗教 或性身份和取向。
### 我们的标准

有助于创造积极环境的行为包括：
•	使用欢迎和包容的语言
•	尊重不同的观点和经验
•	优雅地接受建设性的批评
•	关注什么对社区最有利
•	对其他社区成员表示同情
参与者的不可接受行为包括：
•	使用性意味的语言或意象以及不受欢迎的性注意或者更过分的行为
•	煽动、侮辱/贬损评论以及个人或政治攻击
•	公开或私下骚扰
•	未经明确许可，发布他人的私人信息，如物理或电子地址。
•	在专业场合被合理认为不适当的其他行为

### 我们的责任
维护人员负责澄清可接受行为的标准，并应针对任何不可接受行为采取适当和公平的 纠正措施。
维护人员有权和责任删除、编辑或拒绝与本行为准则不一致的评论、承诺、代码、 wiki编辑、问题和其他贡献，或暂时或永久禁止任何贡献者从事他们认为不适当、 威胁、冒犯或有害的其他行为。
### 范围

当个人代表项目或其社区时，本行为准则既适用于项目空间，也适用于公共空间。 代表一个项目或社区的例子包括使用一个正式的项目电子邮件地址，通过一个正式 的社交媒体帐户发布，或者在在线或离线事件中担任指定的代表。项目维护人员可以 进一步定义和澄清项目的表示。
### 执行
可以通过 17336462189@163.com 联系项目团队来报告辱骂、骚扰或其他不可接受的行为。所有投诉都将被审查和调查，并将产生被认为必要且适合具体情况的回应。项目团队有义务对事件的报告者保密。具体执行政策的更多细节可能会单独发布。
不善意遵守或执行行为准则的项目维护者可能会面临由项目领导的其他成员确定的临时或永久影响。
### 归属
本行为准则改编自《贡献者契约》，版本1.4，可从 https://www.contributor-covenant.org/version/1/4/code-of-conduct.html 获取。

