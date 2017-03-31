# CSS 图像拼合技术 #
## 图像拼合 ##
图像拼合就是单个图像的集合。
有许多图像的网页可能需要很长的时间来加载和生成多个服务器的请求。
使用图像拼合会降低服务器的请求数量，并节省带宽。
## 图像拼合 - 简单实例 ##
与其使用三个独立的图像，不如我们使用这种单个图像（"img_navsprites.gif"）：
navigation images
有了CSS，我们可以只显示我们需要的图像的一部分。
在下面的例子CSS指定显示 "img_navsprites.gif" 的图像的一部分：
实例
img.home
{
width:46px;
height:44px;
background:url(img_navsprites.gif) 0 0;
}
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  img.home {
      width: 46px;
      height: 44px;
      background: url(/images/img_navsprites.gif) 0 0;
  }
  img.next {
      width: 43px;
      height: 44px;
      background: url(/images/img_navsprites.gif) -91px 0;
  }
  </style>
  </head>
  <body>
  <img class="home" src="/images/img_trans.gif"><br>
  //src因为不能为空，所以直接给了他一个透明的图像，然后具体图像由上面给出
  <br>
  <img class="next" src="/images/img_trans.gif">
  </body>
  </html>
<img class="home" src="img_trans.gif" /> -因为不能为空,src属性只定义了一个小的透明图像。显示的图像将是我们在CSS中指定的背景图像
宽度：46px;高度：44px; - 定义我们使用的那部分图像
background:url(img_navsprites.gif) 0 0; - 定义背景图像和它的位置（左0px，顶部0px）
这是使用图像拼合最简单的方法，现在我们使用链接和悬停效果。
//然后具体说明一下，这个背景图片其实是一张很大的图片，然后不断的重复，然后他只是截取了其中的一部分，如果你不规定他的大小框架等等他就不显示， 0 0是具体定位
## 图像拼合 - 创建一个导航列表 ##
我们想使用拼合图像 ("img_navsprites.gif")，以创建一个导航列表。
我们将使用一个HTML列表，因为它可以链接，同时还支持背景图像：
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  #navlist {
      position: relative;
  }
  #navlist li {
      margin: 0;
      padding: 0;
      list-style: none;
      position: absolute;
      top: 0;
  }
  #navlist li, #navlist a {
      height: 44px;
      display: block;
  }
  #home {
      left: 0px;
      width: 46px;
  }
  #home {
      background: url('/images/img_navsprites.gif') 0 0;
  }
  #prev {
      left: 63px;
      width: 43px;
  }
  #prev {
      background: url('/images/img_navsprites.gif') -47px 0;
  }
  #next {
      left: 129px;
      height: 100px;
      width: 43px;
  }
  #next {
      background: url('/images/img_navsprites.gif') -91px 0;
  }
  </style>
  </head>
  
  <body>
  <ul id="navlist">
    <li id="home"><a href="/"></a></li>
    <li id="prev"><a href="/css/"></a></li>
    <li id="next"><a href="/css/"></a></li>
  </ul>
  </body>
  </html>
实例
1. #navlist{position:relative;}
1. #navlist li{margin:0;padding:0;list-style:none;position:absolute;top:0;}
1. #navlist li, #navlist a{height:44px;display:block;}
1. 
1. #home{left:0px;width:46px;}
1. #home{background:url('img_navsprites.gif') 0 0;}
1. 
1. #prev{left:63px;width:43px;}
1. #prev{background:url('img_navsprites.gif') -47px 0;}
1. 
1. #next{left:129px;width:43px;}
1. #next{background:url('img_navsprites.gif') -91px 0;}
实例解析：
1. #navlist{position:relative;} - 位置设置相对定位，让里面的绝对定位
1. #navlist li{margin:0;padding:0;list-style:none;position:absolute;top:0;} - margin和padding设置为0，列表样式被删除，类似于1,2，3这样的，所有列表项是绝对定位
1. #navlist li, #navlist a{height:44px;display:block;} - 所有图像的高度是44px，这里竟然确定了链接的大小，原来链接的大小靠这个确定，然后图像又是靠class，其实不是专业，也可以直接指定class的宽度，然后给他背景，这是可以理解的，同理链接，但是操作的时候一定是需要a:hover 的，所以说，最好全部写成链接
现在开始每个具体部分，的定位和样式：
1. #home{left:0px;width:46px;} - 定位到最左边的方式，以及图像的宽度是46px
1. #home{background:url(img_navsprites.gif) 0 0;} - 定义背景图像和它的位置（左0px，顶部0px）//每个链接都要重新定义背景图片，每个图片都是需要拼接
1. #prev{left:63px;width:43px;} - 右侧定位63px（＃home宽46px+项目之间的一些多余的空间），宽度为43px。
1. #prev{background:url('img_navsprites.gif') -47px 0;} - 定义背景图像右侧47px（＃home宽46px+分隔线的1px）
1. #next{left:129px;width:43px;}- 右边定位129px(#prev 63px + #prev宽是43px + 剩余的空间), 宽度是43px.
1. #next{background:url('img_navsprites.gif') no-repeat -91px 0;} - 定义背景图像右边91px（＃home 46px+1px的分割线+＃prev宽43px+1px的分隔线）
##  图像拼合s - 悬停效果 ##
现在，我们希望我们的导航列表中添加一个悬停效果。
lamp	:hover 选择器用于鼠标悬停在元素上的显示的效果

提示： :hover 选择器可以运用于所有元素。
我们的新图像 ("img_navsprites_hover.gif") 包含三个导航图像和三幅图像：
因为这是一个单一的图像，而不是6个单独的图像文件，当用户停留在图像上不会有延迟加载。
我们添加悬停效果只添加三行代码：
1#home a:hover{background: url('img_navsprites_hover.gif') 0 -45px;}
1#prev a:hover{background: url('img_navsprites_hover.gif') -47px -45px;}
1#next a:hover{background: url('img_navsprites_hover.gif') -91px -45px;}
由于该列表项包含一个链接，我们可以使用：hover伪类
1#home a:hover{background: transparent url(img_navsprites_hover.gif) 0 -45px;} - 对于所有三个悬停图像，我们指定相同的背景位置，只是每个再向下45px