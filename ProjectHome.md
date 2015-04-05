KagariProject

终于想起来填这个坑了，看看过去的一年时光，哎，真的不是能等的啊！
KagariProject是一个开源的基于PHP的弹幕网站框架。鉴于最近沉迷Node.js的我，不排除把它移植到js上的可能。
播放器采用的开源弹幕播放器——MukioPlayer，googlecode地址：http://code.google.com/p/mukioplayer

基本结构
既然是做成框架的话就必然使用MVC模型，但是既然是个小项目的话又没有使用的必要。
controller部分
视频（Video）模块
视频上传upload
视频播放play
视频编辑edit
视频删除delete
视频弹幕下载downloadbulletcomment
视频评分score
评论（Comment）模块
发送评论send
删除评论delete
用户（User）模块
用户登录login
用户注册register
用户资料修改modifyprofile
用户答题answer // B站的你够了！！！
管理模块（Manage）模块
暂时没想好……先不写了……
统计模块（Statics）
貌似没有什么具体的方法
model部分
弹幕格式
弹幕格式是xml实现的，但是json如此流行的情况下，为何不用json来实现呢？
但是我不是很懂ActionScript，所以不太可能修改播放器的代码使之能接受json格式的数据
总之先用着xml的吧
然后就涉及到弹幕缓存的问题，虽然弹幕平时储存在数据库中，但是必要的时候可以使用文件缓存来加速弹幕加载

网站文件结构
index.php // 入口文件
/video // 用于储存视频文件
/cache // 文件缓存
/common // 常用库

数据表设计
video表 //储存视频信息
视频编号vid 视频标题vtitle 视频描述vdes 播放次数playtime 评论数