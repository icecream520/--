Bootstrap将会根据你的屏幕的大小来调整HTML元素的大小————强调响应式设计
深蓝色btn-primary是你的应用的主要颜色，被用在那些用户主要采取的操作上。
Bootstrap自带了一些预定义的按钮颜色。浅蓝色 btn-info 被用在那些用户可能会采取的操作上
Bootstrap自带了一些预定义的按钮颜色。红色btn-danger被用来提醒用户该操作具有“破坏性”，例如删除一张猫的图片。
an image illustrating Bootstrap's grid system
请注意，在这张图表中，class属性 col-md-* 正被使用。在这里，md 表示 medium (中等的)，* 代表一个数字，它指定了这个元素所占的列宽。通过此图表的属性设置可知，在中等大小的屏幕上(例如笔记本电脑)，元素的列宽被指定了。

在我们创建的 Cat Photo App 中，将会使用 col-xs-* ，其中 xs 是 extra small 缩写（应用于较小的屏幕，比如手机屏幕），* 是你需要填写的数字，代表在一行中,各个元素应该占的列宽。

把 Like, Info 和 Delete 三个按钮一并放入一个 <div class="row"> 元素中；然后，其中的每一个按钮都需要各自被一个 <div class="col-xs-4"> 元素包裹。

当div 元素设置了 class 属性 row 之后，那几个按钮便可嵌入其中。

Font Awesome 是一个非常方便的图标库。这些图标都是矢量图形，被保存在 .svg 的文件格式中。这些图标就和字体一样，你可以通过像素单位指定它们的大小，它们将会继承其父HTML元素的字体大小。

你可以将 Font Awesome 图标库增添至任何一个应用中，方法很简单，只需要在你的 HTML 头部增加下列代码即可：

<link rel="stylesheet" href="//cdn.bootcss.com/font-awesome/4.2.0/css/font-awesome.min.css"/>

Bootstrap 有一个 class 属性叫做 well，它的作用是为设定的列创造出一种视觉上的深度感（一种视觉上的效果，动手写代码体会一下）。

在你的每一个class为col-xs-6的div 元素中都嵌入一个带有 well class 属性的 div 元素。