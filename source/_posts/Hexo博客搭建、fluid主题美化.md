---

title: Hexo博客搭建、fluid主题美化
date: 2020-08-28 13:50:05
tags: 
  - 原创
  - fluid
index_img: /img/index/6.jpg
categories: Hexo博客
abbrlink: 1881
---

## 一、添加一言
**1、文章参考地址：**
[https://pxxyyz.com/posts/30454/](https://pxxyyz.com/posts/30454/)

**2、主页效果**
[https://whitejiang.gitee.io/](https://whitejiang.gitee.io/)

**3、替换layout\_partial\plugins目录下的typed.ejs**

``` html
<% if(theme.fun_features.typing.enable && page.subtitle !== false){ %>
  <%- js_ex(theme.static_prefix.typed, "/typed.min.js") %>
  <script>
    function typing(id, title){
        var typed = new Typed('#' + id, {
            strings: [
              '  ',
              title + "&nbsp;",
            ],
            cursorChar: "<%- theme.fun_features.typing.cursorChar %>",
            typeSpeed: <%- theme.fun_features.typing.typeSpeed %>,
            loop: <%- theme.fun_features.typing.loop %>,
        });
        typed.stop();
        $(document).ready(function () {
            $(".typed-cursor").addClass("h2");
            typed.start();
        });
    }
    <% if(is_post()) { %>
        typing("subtitle", "<%- data.subtitle %>")
    <% } else if(theme.index.hitokoto.enable && !page.layout){ %>
        fetch('https://v1.hitokoto.cn')
        .then(response => response.json())
        .then(data => {
           typing("hitokoto", data.hitokoto  + '<br /> <br /> <h4>'+ '——' + '《' + data.from + '》' + '</h4>')
        })
        .catch(console.error)
    <% } else { %>
        typing("subtitle", "<%- data.subtitle %>")
    <% } %>
  </script>
<% } %>
```
**4、修改layout目录下的layout.ejs，**

```javascript

<span class="h2" id="subtitle">


 <!-- 一言 -->
<% if(!is_post()) { %>
<br>
<span class="h2" id="hitokoto">
    <% if(theme.fun_features.typing.enable == false) { %>
    <%- hitokoto %>
    <% } %>
</span>
<% } %>


<% if(is_post()) { %>
```
**5、修改主题配置文件_config.yml，在index下设置hitokoto的开关**

```javascript
#---------------------------
# 首页
# Index Page
#---------------------------
index:
  hitokoto:  # 非post页面显示一言
    enable: true  # slogan 和 hitokoto 不能同时启用，优先显示
```

