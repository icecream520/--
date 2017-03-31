# CSS Positioning(定位) #
定位有时很棘手！
决定显示在前面的元素！
元素可以重叠！
Positioning(定位)
CSS定位属性允许你为一个元素定位。它也可以将一个元素放在另一个元素后面，并指定一个元素的内容太大时，应该发生什么。
元素可以使用的顶部，底部，左侧和右侧属性定位。然而，这些属性无法工作，除非是先设定position属性。他们也有不同的工作方式，这取决于定位方法.
有四种不同的定位方法。
## Static 定位 ##
HTML元素的默认值，即没有定位，元素出现在正常的流中。
静态定位的元素不会受到top, bottom, left, right影响。
## Fixed 定位 ##
元素的位置相对于浏览器窗口是固定位置。
即使窗口是滚动的它也不会移动：
实例
p.pos_fixed
{
position:fixed;
top:30px;
right:5px;
}
注意： Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持.
Fixed定位使元素的位置与文档流无关，因此不占据空间。
Fixed定位的元素和其他元素重叠。
## Relative 定位 ##
相对定位元素的定位是相对其正常位置。//就是说本来正常靠边的，你用这个是相对于其正常位置的
实例
h2.pos_left
{
position:relative;
left:-20px;
}
h2.pos_right
{
position:relative;
left:20px;
}
可以移动的相对定位元素的内容和相互重叠的元素，它原本所占的空间不会改变。//就是说人走人地还要留下
实例
h2.pos_top
{
position:relative;
top:-50px;
}
## Absolute 定位 ##
绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于<html>:
实例
h2
{
position:absolute;
left:100px;
top:150px;
}
Absolutely定位使元素的位置与文档流无关，因此不占据空间。
Absolutely定位的元素和其他元素重叠。
## 重叠的元素 ##
元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素
z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）
一个元素可以有正数或负数的堆叠顺序：
实例
img
{
position:absolute;
left:0px;
top:0px;
z-index:-1;//类似于优先顺序
}
具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。
注意： 如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。
img 
{
	position:absolute;
	clip:rect(0px,60px,200px,0px);
}//裁剪元素
div.scroll
{
	background-color:#00FFFF;
	width:100px;
	height:100px;
	overflow:scroll;//可以滚动
}

div.hidden 
{
	background-color:#00FF00;
	width:100px;
	height:100px;
	overflow:hidden;
}
overflow:auto;
设置浏览器来自动处理溢出。
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    </head>
    <body>
    <p>将鼠标移动到这些字上改变鼠标样式cursor.</p>
    <span style="cursor:auto">auto</span><br>
    <span style="cursor:crosshair">crosshair</span><br>
    <span style="cursor:default">default</span><br>
    <span style="cursor:e-resize">e-resize</span><br>
    <span style="cursor:help">help</span><br>
    <span style="cursor:move">move</span><br>
    <span style="cursor:n-resize">n-resize</span><br>
    <span style="cursor:ne-resize">ne-resize</span><br>
    <span style="cursor:nw-resize">nw-resize</span><br>
    <span style="cursor:pointer">pointer</span><br>
    <span style="cursor:progress">progress</span><br>
    <span style="cursor:s-resize">s-resize</span><br>
    <span style="cursor:se-resize">se-resize</span><br>
    <span style="cursor:sw-resize">sw-resize</span><br>
    <span style="cursor:text">text</span><br>
    <span style="cursor:w-resize">w-resize</span><br>
    <span style="cursor:wait">wait</span><br>
    </body>
    </html>
## 所有的CSS定位属性 ##
"CSS" 列中的数字表示哪个CSS(CSS1 或者CSS2)版本定义了该属性。
属性	说明	值	CSS
bottom	定义了定位元素下外边距边界与其包含块下边界之间的偏移。	auto
length
%
inherit	2
clip	剪辑一个绝对定位的元素	shape
auto
inherit	2
cursor	显示光标移动到指定的类型	url
auto
crosshair
default
pointer
move
e-resize
ne-resize
nw-resize
n-resize
se-resize
sw-resize
s-resize
w-resize
text
wait
help	2
left	定义了定位元素左外边距边界与其包含块左边界之间的偏移。	auto
length
%
inherit	2
overflow
设置当元素的内容溢出其区域时发生的事情。	auto
hidden
scroll
visible
inherit	2
overflow-y
指定如何处理顶部/底部边缘的内容溢出元素的内容区域	auto
hidden
scroll
visible
no-display
no-content	2
overflow-x
指定如何处理右边/左边边缘的内容溢出元素的内容区域	auto
hidden
scroll
visible
no-display
no-content	2
position	指定元素的定位类型	absolute
fixed
relative
static
inherit	2
right	定义了定位元素右外边距边界与其包含块右边界之间的偏移。	auto
length
%
inherit	2
top	定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。	auto
length
%
inherit	2
z-index	设置元素的堆叠顺序	number
auto
inherit	2