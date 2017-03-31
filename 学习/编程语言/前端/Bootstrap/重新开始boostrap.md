## 移动设备优先 ##
为了让 Bootstrap 开发的网站对移动设备友好，确保适当的绘制和触屏缩放，需要在网页的 head 之中添加 viewport meta 标签，如下所示：
<meta name="viewport" content="width=device-width, initial-scale=1.0">
width 属性控制设备的宽度。假设您的网站将被带有不同屏幕分辨率的设备浏览，那么将它设置为 device-width 可以确保它能正确呈现在不同设备上。
initial-scale=1.0 确保网页加载时，以 1:1 的比例呈现，不会有任何的缩放。
在移动设备浏览器上，通过为 viewport meta 标签添加 user-scalable=no 可以禁用其缩放（zooming）功能。
通常情况下，maximum-scale=1.0 与 user-scalable=no 一起使用。这样禁用缩放功能后，用户只能滚动屏幕，就能让您的网站看上去更像原生应用的感觉。
注意，这种方式我们并不推荐所有网站使用，还是要看您自己的情况而定！
<meta name="viewport" content="width=device-width, 
                                     initial-scale=1.0, 
                                     maximum-scale=1.0, 
                                     user-scalable=no">
## 响应式图像 ##
<img src="..." class="img-responsive" alt="响应式图像">
通过添加 img-responsive class 可以让 Bootstrap 3 中的图像对响应式布局的支持更友好。
在下面的代码中，可以看到img-responsive class 为图像赋予了 max-width: 100%; 和 height: auto; 属性，可以让图像按比例缩放，不超过其父元素的尺寸。
.img-responsive {
  display: inline-block;
  height: auto;
  max-width: 100%;
}
这表明相关的图像呈现为 inline-block。当您把元素的 display 属性设置为 inline-block，元素相对于它周围的内容以内联形式呈现，但与内联不同的是，这种情况下我们可以设置宽度和高度。
设置 height:auto，相关元素的高度取决于浏览器。
设置 max-width 为 100% 会重写任何通过 width 属性指定的宽度。这让图片对响应式布局的支持更友好。

inline 与inline-block 不同的是后面的不仅内联还可以设置高度和宽度
## 全局显示、排版和链接 ##
基本的全局显示
Bootstrap 3 使用 body {margin: 0;} 来移除 body 的边距。
请看下面有关 body 的设置：
body {
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 14px;
  line-height: 1.428571429;
  color: #333333;
  background-color: #ffffff;
}
第一条规则设置 body 的默认字体样式为 "Helvetica Neue", Helvetica, Arial, sans-serif。
第二条规则设置文本的默认字体大小为 14 像素。
第三条规则设置默认的行高度为 1.428571429。
第四条规则设置默认的文本颜色为 #333333。
最后一条规则设置默认的背景颜色为白色。

## 排版 ##
使用 @font-family-base、 @font-size-base 和 @line-height-base 属性作为排版样式。
## 
链接样式 ##
通过属性 @link-color 设置全局链接的颜色。
对于链接的默认样式，如下设置：
a:hover,
a:focus {
  color: #2a6496;
  text-decoration: underline;
}

a:focus {
  outline: thin dotted #333;
  outline: 5px auto -webkit-focus-ring-color;
  outline-offset: -2px;
}
所以，当鼠标悬停在链接上，或者点击过的链接，颜色会被设置为 #2a6496。同时，会呈现一条下划线。
除此之外，点击过的链接，会呈现一个颜色码为 #333 的细的虚线轮廓。另一条规则是设置轮廓为 5 像素宽，且对于基于 webkit 浏览器有一个 -webkit-focus-ring-color 的浏览器扩展。轮廓偏移设置为 -2 像素。
以上所有这些样式都可以在 scaffolding.less 中找到。


## 容器（Container） ##
<div class="container">
  ...
</div>
Bootstrap 3 的 container class 用于包裹页面上的内容。让我们一起来看看 bootstrap.css 文件中的这个 .container class。
.container {
   padding-right: 15px;
   padding-left: 15px;
   margin-right: auto;
   margin-left: auto;
}
通过上面的代码，把 container 的左右外边距（margin-right、margin-left）交由浏览器决定。
请注意，由于内边距（padding）是固定宽度，默认情况下容器是不可嵌套的。
.container:before,
.container:after {
  display: table;
  content: " ";
}
这会产生伪元素。设置 display 为 table，会创建一个匿名的 table-cell 和一个新的块格式化上下文。:before 伪元素防止上边距崩塌，:after 伪元素清除浮动。
如果 conteneditable 属性出现在 HTML 中，由于一些 Opera bug，围绕上述元素创建一个空格。这可以通过使用 content: " " 来修复。
.container:after {
  clear: both;
}
它创建了一个伪元素，并确保了所有的容器包含所有的浮动元素。
Bootstrap 3 CSS 有一个申请响应的媒体查询，在不同的媒体查询阈值范围内都为 container 设置了max-width，用以匹配网格系统。
@media (min-width: 768px) {
   .container {
      width: 750px;
}

## Bootstrap 网格系统 ##
响应式网格系统随着屏幕或视口尺寸增加,系统最多分成12列。
## Bootstrap 网格系统（Grid System）的工作原理 ##
行必须放置在.container class内，以获得适当的对齐和内边距.
使用行来创建列的水平组。
内容应该放置在列内,且唯有列可以使行的直接子元素。
预定义的网格类,比如.row和.col-xs-4,可用于快速创建网格布局。LESS混合类可用于更多语义布局。
列通过内边距padding来创建列内容之间的间隙。该内边距是通过.rows上的外边距取负,表示第一列和最后一列的行偏移。
网格系统是通过想要横跨的十二个可用的列来创建的要创建三个相等的列,使用三个.col-xs-4。
## 媒体查询 ##
/* 超小设备（手机，小于 768px） */
/* Bootstrap 中默认情况下没有媒体查询 */

/* 小型设备（平板电脑，768px 起） */
@media (min-width: @screen-sm-min) { ... }

/* 中型设备（台式电脑，992px 起） */
@media (min-width: @screen-md-min) { ... }

/* 大型设备（大台式电脑，1200px 起） */
@media (min-width: @screen-lg-min) { ... }
媒体查询有两个部分，先是一个设备规范，然后是一个大小规则。在上面的案例中，设置了下列的规则：
让我们来看下面这行代码：
@media (max-width: @screen-xs-max) { ... }
@media (min-width: @screen-sm-min) and (max-width: @screen-sm-max) { ... }
@media (min-width: @screen-md-min) and (max-width: @screen-md-max) { ... }
@media (min-width: @screen-lg-min) { ... }
@media (min-width: @screen-sm-min) and (max-width: @screen-sm-max) { ... }

## 基本的网格结构 ##
下面是 Bootstrap 网格的基本结构：
<div class="container">
   <div class="row">
      <div class="col-*-*"></div>
      <div class="col-*-*"></div>      
   </div>
   <div class="row">...</div>
</div>
<div class="container">....

## 偏移列 ##
偏移是一个用于更专业的布局的有用功能。它们可用来给列腾出更多的空间。例如，.col-xs=* 类不支持偏移，但是它们可以简单地通过使用一个空的单元格来实现该效果。
为了在大屏幕显示器上使用偏移，请使用 .col-md-offset-* 类。这些类会把一个列的左外边距（margin）增加 * 列，其中 * 范围是从 1 到 11。
在下面的实例中，我们有 <div class="col-md-6">..</div>，我们将使用 .col-md-offset-3 class 来居中这个 div。
实例
<div class="container">
    <h1>Hello, world!</h1>
    <div class="row" >
        <div class="col-xs-6 col-md-offset-3">//偏移三列 
        style="background-color: #dedef8;box-shadow: 
        inset 1px -1px 1px #444, inset -1px 1px 1px #444;">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing 
            elit.
            </p>
        </div>
    </div>
</div>

## 嵌套列 ##
为了在内容中嵌套默认的网格，请添加一个新的 .row，并在一个已有的 .col-md-* 列内添加一组 .col-md-* 列。被嵌套的行应包含一组列，这组列个数不能超过12（其实，没有要求你必须占满12列）。
在下面的实例中，布局有两个列，第二列被分为两行四个盒子。
## 列排序 ##
Bootstrap 网格系统另一个完美的特性，就是您可以很容易地以一种顺序编写列，然后以另一种顺序显示列。
您可以很轻易地改变带有 .col-md-push-* 和 .col-md-pull-* 类的内置网格列的顺序，其中 * 范围是从 1 到 11。
在下面的实例中，我们有两列布局，左列很窄，作为侧边栏。我们将使用 .col-md-push-* 和 .col-md-pull-* 类来互换这两列的顺序。