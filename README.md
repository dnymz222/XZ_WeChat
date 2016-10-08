# XZ_WeChat

博客介绍地址：[戳这里](http://coderperson.com/2016/09/28/iOS-weChat/)

效果图展示：			
![1](http://img.blog.csdn.net/20160928230616321)		
![2](http://img.blog.csdn.net/20160928230519993)		



做了两年IM相关工作了，去年是集成环信的SDK实现的IM功能，今年公司拥有自己的长连接服务器，于是从头自己定协议然后一步步实现了IM的整体功能，基本把微信IM有关的内容都实现了。最近开始整理过去的一些知识，于是先从聊天框架下手，我从项目中抽出这个简易的聊天框架，方便大家学习交流。			


由于该框架是我用最快的时间从原项目中抽出来的，摘除了本地缓存的功能（这部分内容太多了），所以里面或多或少有一些我原项目中的业务逻辑，不过不要紧，这不会影响你对聊天框架的学习，我也会逐渐把该框架规范起来。		

由于作者的电脑环境被折腾坏了，不能安装cocoapods来管理一些用到的三方，所以直接导入进了该框架，这一点大家不要学习。


该框架目前支持的消息类型：文本消息（包含表情），图片消息，语音消息，视频消息，文件消息(pdf,word,excel,ppt,png,html等格式)。

如果你想展示文件消息，你需要把文件拷贝到沙盒的`/Library/Caches/Chat/File`目录下,由于我以前是从PC端发送文件到手机端进行的展示，所以目前只能你手动拷贝了。

项目中展示的视频已经转成了`mp4`类型，而且也经过了压缩，语音也转换成了`amr`格式，节省流量的同时，可以和安卓端兼容。


你能从该框架学习到什么：		

* 聊天框架的搭建
* 表情键盘的实现
* 语音相关的知识
* 视频相关的知识
* 文件相关的功能
* 转场动画相关的知识
* 数据模型和尺寸模型分离
* 你能清楚的了解到在实战项目中IM的实现	


目前该框架这是初步，我还有好多功能没有加入进去，后续会慢慢加入，包括：		
* 消息的转发、拷贝、撤回
* 文章的分享
* 订阅号的功能
* 红包的功能
* 本地缓存的功能(其实很多功能都要基于数据库的，我把数据库去除掉后，很多功能就一块去除了)
* 草稿箱的功能
* 等等等还有好多好多


---

**更新日志**：			

10月8日：添加了消息的拷贝、删除、撤回功能，由于转发功能需要用到数据库所以我只添加了转发的UI,等添加了数据库后再完善。`注意`这里的只有自己的消息并且是发送成功的消息才可以撤回，我这里限制的是`5分钟`内的消息可以撤回,超过规定时间不允许撤回。





如果你在学习过程中有什么问题可以和我留言，大家共同提高。如果该框架能帮助到你，欢迎star，你的关注是我最大的动力，谢谢！




