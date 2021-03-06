---
layout: post
title:  "博客新主题"
categories: [sticky]
tags: Jekyll 博客
comments: true
share: true
---

终于切到了新主题，jekyll 也升级到了 3.x

源码地址：[github.com/mdluo/mdluo.github.io](https://github.com/mdluo/mdluo.github.io)，也可点击右上角 GitHub 图标跳转

主题主要部分基于 [end2end](https://github.com/nandomoreirame/end2end)，文章内容样式参考 [Kiko](https://github.com/gfjaru/Kiko)

调整优化移动设备显示效果：屏幕较小时隐藏右上角 GitHub 图标及部分分享图标、调整代码块字体

使用 [Real Favicon Generator](http://realfavicongenerator.net/) 生成的多媒体适配 favicon，以及微信分享图标（在页面中加入隐藏的尺寸大于 290 px 的图片）

调整多行代码块在设置行号的情况下的显示效果，效果在下方

添加置顶文章，方法参考：[Jekyll: Making Posts Sticky](http://swaac.tamouse.org/swaac/2013/09/28/jekyll-making-posts-sticky/)

静态资源使用 [七牛](http://www.qiniu.com/) (qiniu) 云存储 和 [又拍云](https://www.upyun.com) (upyun) 融合 CDN 加速并全部开启 HTTPS

添加对 IE 9 及以下版本浏览器排版支持，但是在页面顶部显示建议升级浏览器的提醒

开启了全站 HTTPS，方法是在 `_config.yml` 中设置 `enforce_ssl: mdluo.github.io`，并在页面头部加入判断代码：

{% highlight js linenos %}
var host = "{{ site.enforce_ssl }}";
if ((host == window.location.host) && (window.location.protocol != "https:"))
  window.location.protocol = "https";
{% endhighlight %}

域名换回 `mdluo.github.io`，防止自己的域名被墙，同时也可以使用 [Git.io](https://git.io/) 为博客设置短 URL

底部个人社交媒体图标来自网上的 SVG 并进行了调整统一样式，加上了网站的颜色

文章详情页底部使用了 CC-BY 的 SVG 图标以及 [share.js](http://overtrue.me/share.js/) 做分享到社交媒体图标

背景使用了 [Dimitrie Hoekstra](http://dhesign.com/) 制作的 [GPlay](http://subtlepatterns.com/gplay/)，更多背景样式可以在 [Subtle Patterns](http://subtlepatterns.com/) 上找到

**Todos:**

- 完善 About、Tags、Wikis 页面
- License 文件及 About 页面加上引用的第三方内容的版权信息
- 参考 [onepice](https://github.com/guovz/onepice)、[Neo-HPSTR](https://github.com/aron-bordin/neo-hpstr-jekyll-theme)、[Scribble](https://github.com/muan/scribble)、[dbyll](https://github.com/dbtek/dbyll) 等主题为博客添加 Tag 页面、前后文章切换、作者信息、焦点图、回到顶部等功能
