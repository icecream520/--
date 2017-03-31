nav 标签定义及使用说明
<nav> 标签定义导航链接的部分。
并不是所有的 HTML 文档都要使用到 <nav> 元素。<nav> 元素只是作为标注一个导航链接的区域。
在不同设备上（手机或者PC）可以制定导航链接是否显示，以适应不同屏幕的需求。排序其实就是改变列的方向，也就是改变左右浮动，并且设置浮动的距离。在栅格系统里，可以通过.col-md-push-*和.col-md-pull-*来实现这一目的。先来看看效果示意图，如图2-6所示。

<template>声明模板元素

<card>卡片只要求少量的标记以及类，就能为你提供尽可能多的控件。这些类和标记很灵活，通常可以轻松地重新混合和扩展
<jumbotron>超大屏幕 。顾名思义该组件可以增加标题的大小，并为登陆页面内容添加更多的外边距（margin）
bootstrap-flex
<media>媒体对象 类似 ![这样的](http://i.imgur.com/w1ixmmo.png) 一种媒体风格
class="media" 容纳媒体对象的所有内容
class="media-object" 媒体对象,常常是图片
class="media-body" 媒体中的主体内容,常常是图片侧边内容
media-heading 对象标题

3、媒体对象–媒体对象列表
媒体对象的嵌套仅是媒体对象中一个简单应用效果之一，在很多时候，我们还会碰到一个列表，每个列表项都和媒体对象长得差不多，同样用评论系统来说事：![例如这个图片](http://i.imgur.com/0dtZfRN.jpg)
<ul class="media-list">
 <li class="media">
  <a class="pull-left" href="#">
   <img class="media-object" src=" " alt="...">
  </a>
  <div class="media-body">
   <h4 class="media-heading">Media Header</h4>
   <div>…</div>
  </div>
 </li>
 <li class="media">…</li>
 <li class="media">…</li>
</ul>


表单：

form-group 获取最佳间距