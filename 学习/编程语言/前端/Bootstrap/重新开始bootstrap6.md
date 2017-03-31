# Bootstrap 响应式实用工具 #
	超小屏幕
手机 (<768px)	小屏幕
平板 (≥768px)	中等屏幕
桌面 (≥992px)	大屏幕
桌面 (≥1200px)
.visible-xs-*	可见	隐藏	隐藏	隐藏
.visible-sm-*	隐藏	可见	隐藏	隐藏
.visible-md-*	隐藏	隐藏	可见	隐藏
.visible-lg-*	隐藏	隐藏	隐藏	可见
.hidden-xs	隐藏	可见	可见	可见
.hidden-sm	可见	隐藏	可见	可见
.hidden-md	可见	可见	隐藏	可见
.hidden-lg	可见	可见	可见	隐藏
<div class="container" style="padding: 40px;">
    <div class="row visible-on">
        <div class="col-xs-6 col-sm-3" style="background-color: #dedef8;
        box-shadow: inset 1px -1px 1px #444, inset -1px 1px 1px #444;">
            <span class="hidden-xs">特别小型</span>
            <span class="visible-xs">✔ 在特别小型设备上可见</span>
        </div>
        <div class="col-xs-6 col-sm-3" style="background-color: #dedef8;
        box-shadow: inset 1px -1px 1px #444, inset -1px 1px 1px #444;">
            <span class="hidden-sm">小型</span>
            <span class="visible-sm">✔ 在小型设备上可见</span>
        </div>
        <div class="clearfix visible-xs"></div>
        <div class="col-xs-6 col-sm-3" style="background-color: #dedef8;
        box-shadow: inset 1px -1px 1px #444, inset -1px 1px 1px #444;">
            <span class="hidden-md">中型</span>
            <span class="visible-md">✔ 在中型设备上可见</span>
        </div>
        <div class="col-xs-6 col-sm-3" style="background-color: #dedef8;
        box-shadow: inset 1px -1px 1px #444, inset -1px 1px 1px #444;">
            <span class="hidden-lg">大型</span>
            <span class="visible-lg">✔ 在大型设备上可见</span>
        </div>
    </div>
</div>

# Bootstrap 字体图标(Glyphicons) #
什么是字体图标？
字体图标是在 Web 项目中使用的图标字体。虽然，Glyphicons Halflings 需要商业许可，但是您可以通过基于项目的 Bootstrap 来免费使用这些图标。
为了表示对图标作者的感谢，希望您在使用时加上 GLYPHICONS 网站的链接。

## CSS 规则解释 ##
@font-face {
  font-family: 'Glyphicons Halflings';
  src: url('../fonts/glyphicons-halflings-regular.eot');
  src: url('../fonts/glyphicons-halflings-regular.eot?#iefix') format('embedded-opentype'), url('../fonts/glyphicons-halflings-regular.woff') format('woff'), url('../fonts/glyphicons-halflings-regular.ttf') format('truetype'), url('../fonts/glyphicons-halflings-regular.svg#glyphicons_halflingsregular') format('svg');
}

.glyphicon {
  position: relative;
  top: 1px;
  display: inline-block;
  font-family: 'Glyphicons Halflings';
  -webkit-font-smoothing: antialiased;
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  -moz-osx-font-smoothing: grayscale;
}
所以 font-face 规则实际上是在找到 glyphicons 地方声明 font-family 和位置。
.glyphicon class 声明一个从顶部偏移 1px 的相对位置，呈现为 inline-block，声明字体，规定 font-style 和 font-weight 为 normal，设置行高为 1。除此之外，使用 -webkit-font-smoothing: antialiased 和 -moz-osx-font-smoothing: grayscale; 获得跨浏览器的一致性。
然后，这里的
.glyphicon:empty {
  width: 1em;
}
是空的 glyphicon。
这里有 200 个 class，每个 class 针对一个图标。这些 class 的常见格式如下：
.glyphicon-keyword:before {
  content: "hexvalue";
}
比如，使用的 user 图标，它的 class 如下：
.glyphicon-user:before {
  content: "\e008";
}
## @font-face ##

什么是@font-face，以及在css当中如何使用
@ font-face的是一个CSS规则，允许你输入自己的字体出现在网站上，即使在特定的字体在访问者的计算机上没有安装。这条规则最重要的是，它为设计师打开了一个全新的世界。您可以使用任何你喜欢的字体。
下面的语法是你如何使用@ font-face的。首先，定义新的字体所提供的名称和说明的字体。

@font-face {
    font-family: DeliciousRoman;
    src: url('http://www.font-face.com/fonts/delicious/Delicious-Roman.otf');
}
然后你引用它。

p {
    font-family: DeliciousRoman, Helvetica, Arial, sans-serif;
}
就是这样。

在前面的例子中使用外部来源。但是，如果将字体文件是在您的服务器上，那么你可以参考以下的方式：

@font-face {
    font-family: DeliciousRoman;
    src: url('…/Delicious-Roman.otf');
}
此外，还有其他三个字体属性，您应该知道的。首先是font-stretch，您可以设定的字体会被拉伸，“normal’”是默认的。此外，有字体的风格，让你的字体是斜或斜体。最后，还有字体的重量，最后字体为粗体，等你可以自己设置
下面的语法是你如何使用@ font-face的。首先，定义新的字体所提供的名称和说明的字体。

@font-face {
    font-family: DeliciousRoman;
    src: url('http://www.font-face.com/fonts/delicious/Delicious-Roman.otf');
}
然后你引用它。

p {
    font-family: DeliciousRoman, Helvetica, Arial, sans-serif;
}
就是这样。

在前面的例子中使用外部来源。但是，如果将字体文件是在您的服务器上，那么你可以参考以下的方式：

@font-face {
    font-family: DeliciousRoman;
    src: url('…/Delicious-Roman.otf');
}
此外，还有其他三个字体属性，您应该知道的。首先是font-stretch，您可以设定的字体会被拉伸，“normal’”是默认的。此外，有字体的风格，让你的字体是斜或斜体。最后，还有字体的重量，最后字体为粗体，等你可以自己设置

## 用法 ##
如需使用图标，只需要简单地使用下面的代码即可。请在图标和文本之间保留适当的空间。
<span class="glyphicon glyphicon-search"></span>

<p>
    <button type="button" class="btn btn-default">
        <span class="glyphicon glyphicon-sort-by-attributes"></span>
    </button>
    <button type="button" class="btn btn-default">
        <span class="glyphicon glyphicon-sort-by-attributes-alt"></span>
    </button>
    <button type="button" class="btn btn-default">
        <span class="glyphicon glyphicon-sort-by-order"></span>
    </button>
    <button type="button" class="btn btn-default">
        <span class="glyphicon glyphicon-sort-by-order-alt"></span>
    </button>
</p>
<button type="button" class="btn btn-default btn-lg">
    <span class="glyphicon glyphicon-user"></span>
    User
</button>
<button type="button" class="btn btn-default btn-sm">
    <span class="glyphicon glyphicon-user"></span>
    User
</button>
<button type="button" class="btn btn-default btn-xs">
    <span class="glyphicon glyphicon-user"></span>
    User
</button>

## 带有导航栏的字体图标 ##
<div class="navbar navbar-fixed-top navbar-inverse" role="navigation">
    <div class="container">
        <div class="navbar-header">
            <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
                <span class="sr-only">Toggle navigation</span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
                <span class="icon-bar"></span>
            </button>
            <a class="navbar-brand" href="#">Project name</a>
        </div>
        <div class="collapse navbar-collapse">
            <ul class="nav navbar-nav">
                <li class="active">
                    <a href="#">
                        <span class="glyphicon glyphicon-home">Home</span></a>
                </li>
                <li>
                    <a href="#shop">
                        <span class="glyphicon glyphicon-shopping-cart">Shop</span></a>
                </li>
                <li>
                    <a href="#support">
                        <span class="glyphicon glyphicon-headphones">Support</span></a>
                </li>
            </ul>
        </div>
        <!-- /.nav-collapse -->
    </div>
    <!-- /.container -->
</div>
<!-- jQuery (Bootstrap 插件需要引入) -->
<script src="http://cdn.static.runoob.com/libs/jquery/2.1.1/jquery.min.js"></script>
<!-- 包含了所有编译插件 -->
<script src="http://cdn.static.runoob.com/libs/bootstrap/3.3.7/js/bootstrap.min.js"></script>

## 定制字体图标 ##
我们已经看到如何使用字体图标，接下来我们看看如何定制字体图标。
我们将以上面的实例开始，并通过改变字体尺寸、颜色和应用文本阴影来进行定制图标。
下面是开始的代码：
<button type="button" class="btn btn-primary btn-lg">
  <span class="glyphicon glyphicon-user"></span> User
</button>
## 定制字体尺寸 ##
通过增加或减少图标的字体尺寸，您可以让图标看起来更大或更小。
<button type="button" class="btn btn-primary btn-lg" style="font-size: 60px">
  <span class="glyphicon glyphicon-user"></span> User
</button>

## 应用文本阴影 ##
<button type="button" class="btn btn-primary btn-lg" style="text-shadow: black 5px 3px 3px;">
  <span class="glyphicon glyphicon-user"></span> User
</button>