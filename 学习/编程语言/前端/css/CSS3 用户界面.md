# CSS3 用户界面 #
CSS3 用户界面
在 CSS3 中, 增加了一些新的用户界面特性来调整元素尺寸，框尺寸和外边框。
在本章中，您将了解以下的用户界面属性：
resize
box-sizing
outline-offset
## CSS3 调整尺寸(Resizing) ##
CSS3中，resize属性指定一个元素是否应该由用户去调整大小。
这个 div 元素由用户调整大小。 (在 Firefox 4+, Chrome, 和 Safari中)
CSS代码如下：
OperaSafariChromeFirefoxInternet Explorer
实例
由用户指定一个div元素尺寸大小：
div
{
resize:both;
overflow:auto;
}
## CSS3 方框大小调整(Box Sizing) ##
box-sizing 属性允许您以确切的方式定义适应某个区域的具体内容。
OperaSafariChromeFirefoxInternet Explorer
实例
规定两个并排的带边框方框：
div
{
box-sizing:border-box;
-moz-box-sizing:border-box; /* Firefox */
width:50%;
float:left;
}
SS3 外形修饰（outline-offset ）
outline-offset 属性对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓。
轮廓与边框有两点不同：
轮廓不占用空间
轮廓可能是非矩形
这个 div 在边框之外 15 像素处有一个轮廓。
The CSS code is as follows:
OperaSafariChromeFirefoxInternet Explorer
实例
规定边框边缘之外 15 像素处的轮廓：
div
{
border:2px solid black;
outline:2px solid red;
outline-offset:15px;
}
新的用户界面特性
属性	说明	CSS
appearance	允许您使一个元素的外观像一个标准的用户界面元素	3
box-sizing	允许你以适应区域而用某种方式定义某些元素	3
icon	为创作者提供了将元素设置为图标等价物的能力。	3
nav-down	指定在何处使用箭头向下导航键时进行导航	3
nav-index	指定一个元素的Tab的顺序	3
nav-left	指定在何处使用左侧的箭头导航键进行导航	3
nav-right	指定在何处使用右侧的箭头导航键进行导航	3
nav-up	指定在何处使用箭头向上导航键时进行导航	3
outline-offset	外轮廓修饰并绘制超出边框的边缘	3
resize	指定一个元素是否是由用户调整大小	3