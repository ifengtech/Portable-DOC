# Android第三方开源库收集整理
原文：[http://www.tuicool.com/articles/jyA3MrU](http://www.tuicool.com/articles/jyA3MrU)

标签：`#GitHub` `#开源框架` `#Android`

>首先，就我个人开发经验，总结一下平常用到的一些最常用的功能： 
>
>- 下载，比如图片，文件。
>- 将下载的文件进行解压。
>- 请求服务器，比如说上传登陆信息，更新某些数据，又或者上传头像文件。
>- 从文件系统中选择要操作的文件（图片，拍照，视频，拍摄视频）。
>- 有时候也需要爬取某些网页数据。
>- 存储一些配置信息
>- 播放视频
>- 再有一个特殊需求就是关乎Android程序UI设计，图标是个很麻烦的问题。每次都难以找到合适的Android 设计UI。

## 框架的选择
正如上面提到的，APP开发涉及到的技术包含方方面面。在Github上也有大量的开源框架可供引用，但是如何在这些技术上以及框架上做好选择呢。这很大一部分是根据开发人员的项目经验决定，至于别人的框架程序员则会认为“不一定适合自己的”而予与否认。正好[Appbrain Stats][2]网站可以按照标签查找出自己想要的框架，还可以看到框架被其他APP采用的数据。

[![](1)][2]


## Retrofit [[DOC]](http://square.github.io/retrofit/)
A type-safe REST client for Android and Java

*Introduction*

Retrofit turns your REST API into a Java interface.

	public interface GitHubService {
	  @GET("/users/{user}/repos")
	  List<Repo> listRepos(@Path("user") String user);
	}

The `RestAdapter` class generates an implementation of the `GitHubService` interface.

	RestAdapter restAdapter = new RestAdapter.Builder()
	    .setEndpoint("https://api.github.com")
	    .build();
	
	GitHubService service = restAdapter.create(GitHubService.class);

Each call on the generated `GitHubService` makes an HTTP request to the remote webserver.

	List<Repo> repos = service.listRepos("octocat");

Use annotations to describe the HTTP request:

- URL parameter replacement and query parameter support
- Object conversion to request body (e.g., JSON, protocol buffers)
- Multipart request body and file upload

> REST框架的模式，和springMVC的服务器接口设计框架模式一样。

## 组合动画设计

> 看到为什么别人家的APP，可以设计的那么酷炫，又是怎么做到的呢？
> 比如[Euclid](https://github.com/Yalantis/Euclid)这个DEMO，设计出了新`Activity` BringToFront的系列动画设计。
> 用这个DEMO来学习下面两个框架，深入研究系列动画的设计。


- [NineOldAndroid](http://nineoldandroids.com/)
- [ActionBarSherlock](http://actionbarsherlock.com/)

[1]:https://github.com/ifengtech/Portable-DOC/blob/master/art/appbrain.png
[2]:http://www.appbrain.com/stats/libraries