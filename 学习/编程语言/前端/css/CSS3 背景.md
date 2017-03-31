# CSS3 背景 #
CSS3 背景
CSS3中包含几个新的背景属性，提供更大背景元素控制。
在本章您将了解以下背景属性：
background-image
background-size
background-origin
background-clip
您还将学习如何使用多重背景图像。
##CSS3 background-image属性##CSS3中可以通过background-image属性添加背景图片。
不同的背景图像和图像用逗号隔开，所有的图片中显示在最顶端的为第一张。
实例
#example1 {
background-image: url(img_flwr.gif), url(paper.gif);//第一张第一个
background-position: right bottom, left top;
background-repeat: no-repeat, repeat;
}
可以给不同的图片设置多个不同的属性
实例
#example1 {
background: url(img_flwr.gif) right bottom no-repeat, url(paper.gif) left top repeat;
}
## CSS3 background-size 属性 ##
background-size指定背景图像的大小。CSS3以前，背景图像大小由图像的实际大小决定。
CSS3中可以指定背景图片，让我们重新在不同的环境中指定背景图片的大小。您可以指定像素或百分比大小。
你指定的大小是相对于父元素的宽度和高度的百分比的大小。
实例 1
重置背景图像：
div
{
background:url(img_flwr.gif);
background-size:80px 60px;
background-repeat:no-repeat;
}
实例 2
伸展背景图像完全填充内容区域：
div
{
background:url(img_flwr.gif);
background-size:100% 100%;
background-repeat:no-repeat;
}
## CSS3的background-Origin属性 ##
background-Origin属性指定了背景图像的位置区域。
content-box, padding-box,和 border-box区域内可以放置背景图像。
实例
在 content-box 中定位背景图片：
div
{
background:url(img_flwr.gif);
background-repeat:no-repeat;
background-size:100% 100%;
background-origin:content-box;
}
CSS3 多个背景图像
CSS3 允许你在元素
那个添加多个背景图像。
OperaSafariChromeFirefoxInternet Explorer
实例
在 body 元素中设置两个背景图像：
body
{ 
background-image:url(img_flwr.gif),url(img_tree.gif);
}
## CSS3 background-clip属性 ##
CSS3中background-clip背景剪裁属性是从指定位置开始绘制
实例
#example1 {
border: 10px dotted black;
padding: 35px;
background: yellow;
background-clip: content-box;
}
## 新的背景属性 ##
顺序	描述	CSS
background-clip	规定背景的绘制区域。	3
background-origin	规定背景图片的定位区域。	3
background-size	规定背景图片的尺寸。	3
