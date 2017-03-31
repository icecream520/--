CSS Margin(外边距)属性定义元素周围的空间。
## Margin ##
margin清除周围的元素（外边框）的区域。margin没有背景颜色，是完全透明的
margin可以单独改变元素的上，下，左，右边距。也可以一次改变所有的属性。
可能的值
值	说明
auto	设置浏览器边距。
这样做的结果会依赖于浏览器
length	定义一个固定的margin（使用像素，pt，em等）
%	定义一个使用百分比的边距
Remark Margin可以使用负值，重叠的内容。
<h2Margin - 单边外边距属性
在CSS中，它可以指定不同的侧面不同的边距：
实例
margin-top:100px;
margin-bottom:100px;
margin-right:50px;
margin-left:50px;
Margin - 简写属性
<p为了缩短代码，有可能使用一个属性中margin指定的所有边距属性。这就是所谓的缩写属性。
所有边距属性的缩写属性是"margin"://就是说上下左右同时缩小
实例
margin:100px 50px;
margin属性可以有一到四个值。/p>
margin:25px 50px 75px 100px;
上边距为25px
右边距为50px
下边距为75px
左边距为100px

margin:25px 50px 75px;
上边距为25px
左右边距为50px
下边距为75px

margin:25px 50px;
上下边距为25px
左右边距为50px

margin:25px;
所有的4个边距都是25px
margin:2cm
maggin-top:20%//可以设置百分比及距离上部的cm数
## 所有的CSS边距属性 ##
属性	描述
margin	简写属性。在一个声明中设置所有外边距属性。
margin-bottom	设置元素的下外边距。
margin-left	设置元素的左外边距。
margin-right	设置元素的右外边距。
margin-top	设置元素的上外边距。