---

title: Hexo博客搭建、简洁优雅的fluid主题
date: 2020-08-28 12:55:57
tags: 
    - 原创
    - fluid
index_img: /img/index/5.jpg
categories: Hexo博客
abbrlink: 1771
---

## 一、效果

[https://whitejiang.gitee.io/](https://whitejiang.gitee.io/)

## 二、准备工作

**在开始一切之前，你必须已经：**

**1.有一个github账号或者gitee（码云）账号**

**推荐注册码云账号，网速快**：[https://gitee.com/](https://gitee.com/)

**注：新建仓库时，用户名和仓库名需保持一致，，，**
**原因：生成的默认pages地址好看。**

**2.安装node.js、npm**

**node.js官网**：[http://nodejs.cn/download/](http://nodejs.cn/download/)

**3.安装git**

**git官网**：[https://git-scm.com/](https://git-scm.com/)

## 三、安装hexo

```html
 npm install -g hexo-cli

```

## 四、初始化
**在电脑的某个地方新建一个名为hexo的文件夹（名字可以随便取），
比如我的是D:\Hexo\sunshine，由于这个文件夹将来就作为你存放代码的地方，所以最好不要随便放。**

**在sunshine文件夹下点击右键，点击 Git Bash Here，输入命令**

```html
 hexo init

```
**hexo会自动下载一些文件到这个目录，目录结构如下图：**

![在这里插入图片描述](https://img-blog.csdnimg.cn/2020082721493659.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1cyMTE5NTMzMzI=,size_16,color_FFFFFF,t_70#pic_center)

## 五、部署运行

``` html
 hexo g   
```

``` html
 hexo s  
```
**hexo s是开启本地预览服务，打开浏览器访问 http://localhost:4000 即可看到内容**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200828094939893.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1cyMTE5NTMzMzI=,size_16,color_FFFFFF,t_70#pic_center)


## 六、配置主题
**1、fluid主题下载**：[https://github.com/fluid-dev/hexo-theme-fluid](https://github.com/fluid-dev/hexo-theme-fluid)

**2、解压复制到：D:\Blog\sunshine\themes   目录下，如图：**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200828092552693.jpg#pic_center)

**3、修改  D:\Blog\sunshine  目录下_config.yml**
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200828093012659.jpg#pic_center)



