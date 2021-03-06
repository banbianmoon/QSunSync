﻿# QSunSync 七牛云文件同步工具

## 简单介绍

`QSunSync`是使用`C# + WPF`开发的用于将本地文件同步到七牛云端空间的Windows客户端。该客户端的特点就是简单易用，而且方便增量同步。

## 下载安装

![下载图标](http://devtools.qiniu.com/download.png?imageView2/0/w/16) [QSunSync-v2.1.1](http://devtools.qiniu.com/QSunSync-v2.1.1.zip) 

1. 该软件的使用需要`.NET Framework 4.0`支持，可以从 [微软官方下载中心](https://www.microsoft.com/zh-cn/download/details.aspx?id=17718) 下载安装。  
2. 该软件使用了`SQLite`数据库来记录本地文件的hash值，所以需要在`.NET Framework4.0`安装完成之后，安装`SQLite`支持软件，这个可以从 [这里](
http://devtools.qiniu.com/sqlite_net4.0.exe) 下载，该软件仅仅是一个依赖库，不会对原有系统稳定性造成影响。  
3. 然后下载`QSunSync`解压缩后，双击 `QSunSync.exe` 打开就可以使用了。 

备注：如果使用的是旧版本，请先删除 "我的文档" 目录下的文件夹 `qsunsync` 。

## 功能介绍

该软件支持如下功能：  

1. 可以将指定文件夹中文件完整同步到目标空间，默认以文件在文件夹中的相对路径作为文件名  
2. 可以在上传之前，对空间中同名文件进行检查，如果发现同名文件则根据强制覆盖条件的设置来决定是否覆盖  
3. 可以给上传到空间的文件指定一个额外的前缀    
4. 可以忽略文件名称相对于同步目录的相对路径，直接以文件本身的名字来命名  
5. 可以根据上传的机器位置选择合适的入口域名  
6. 可以根据文件的平均大小和实际带宽设置一个合理的并发数量  
7. 可以根据实际带宽的情况，选择分片上传的片的大小，带宽越大，片大小可以选择越大，效率越高  
8. 支持单文件断点续传，支持目录增量同步

##  自行编译

如果你打算自行编译这个项目的话，请按照如下方式： 
 
1. 这个项目是使用 Visual Studio 2015 开发的，所以这个版本以上的都可以；  
2. 这个项目依赖另外一个项目提供的SDK，这个项目是 [csharp-sdk](https://github.com/qiniu/csharp-sdk)；  
3. 然后，编译吧。  
 

## 使用方式

1. 首次打开软件的时候，需要进行帐号设置才能去“新建同步任务”，七牛云存储的文件上传使用一对密钥`AK/SK`来进行权限校验，这一对密钥在七牛云存储的后台里面是可以找到的。  
2. 你可以直接到“帐号设置”里面点击“查看我的AS&SK”，这将自动帮你打开浏览器并导向到`AK/SK`的所在地，你直接拷贝，粘贴到本地的输入框里面就好了，输入完成之后，点击“保存”
就可以了，当然如果你输入了错误的`AK&SK`，你会收到错误提示的，嘿嘿。  
3. 帐号设置完成之后，就可以“新建同步任务”了，在“同步设置”的“基本设置”里面，你可以选择本地待同步目录和希望同步到的云端空间即可，如果需要更多的设置，可以看“高级设置”。
4. 设置完成之后，你就可以点击“开始同步”进行同步了。  


## 意见&帮助

如果你有任何的意见，可以通过提 issue，我们来讨论。如果你需要帮助，可以加入群 （QQ: 343822521），非技术勿扰。
