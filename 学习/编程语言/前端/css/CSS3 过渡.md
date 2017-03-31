# CSS3 过渡 #
CSS3 过渡
CSS3中，我们为了添加某种效果可以从一种样式转变到另一个的时候，无需使用Flash动画或JavaScript。用鼠标移过下面的元素：
## 它是如何工作？ ##
CSS3 过渡是元素从一种样式逐渐改变为另一种的效果。
要实现这一点，必须规定两项内容：
指定要添加效果的CSS属性
指定效果的持续时间。
它是如何工作？
CSS3 过渡是元素从一种样式逐渐改变为另一种的效果。
要实现这一点，必须规定两项内容：
指定要添加效果的CSS属性
指定效果的持续时间。
实例
应用于宽度属性的过渡效果，时长为 2 秒：
div
{
transition: width 2s;
-webkit-transition: width 2s; /* Safari */
}

注意： 如果未指定的期限，transition将没有任何效果，因为默认值是0。
指定的CSS属性的值更改时效果会发生变化。一个典型CSS属性的变化是用户鼠标放在一个元素上时：
OperaSafariChromeFirefoxInternet Explorer
实例
规定当鼠标指针悬浮(:hover)于 <div>元素上时：
div:hover
{
width:300px;
}
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  div {
      width: 100px;
      height: 100px;
      background: red;
      transition: width 2s;
      //规定这个元素的配置属性，然后设置其形变时间
      -webkit-transition: width 2s; /* Safari */
  }
  div:hover {
      width: 300px;
  }
  </style>
  </head>
  <body>
  <p><b>注意：</b>该实例无法在 Internet Explorer 9 及更早 IE 版本上工作。</p>
  <div></div>
  <p>鼠标移动到 div 元素上，查看过渡效果。</p>
  </body>
  </html>
## 多项改变 ##
要添加多个样式的变换效果，添加的属性由逗号分隔：
OperaSafariChromeFirefoxInternet Explorer
实例
添加了宽度，高度和转换效果：
div
{
transition: width 2s, height 2s, transform 2s;
//一般情况下都要设置完成他的长宽，然后再设置其形变时间，都是由相对应的属性决定的
-webkit-transition: width 2s, height 2s, -webkit-transform 2s;
}
## 过渡属性 ##
下表列出了所有的过渡属性:
属性	描述	CSS
transition	简写属性，用于在一个属性中设置四个过渡属性。	3
transition-property	规定应用过渡的 CSS 属性的名称。	3
transition-duration	定义过渡效果花费的时间。默认是 0。	3
transition-timing-function	规定过渡效果的时间曲线。默认是 "ease"。	3
transition-delay	规定过渡效果何时开始。默认是 0。	3
下面的两个例子设置所有过渡属性：
OperaSafariChromeFirefoxInternet Explorer
实例
在一个例子中使用所有过渡属性：
div
{
transition-property: width;
transition-duration: 1s;
transition-timing-function: linear;
transition-delay: 2s;
/* Safari */
-webkit-transition-property:width;
-webkit-transition-duration:1s;
-webkit-transition-timing-function:linear;
-webkit-transition-delay:2s;
}
实例
与上面的例子相同的过渡效果，但是使用了简写的 transition 属性：
div
{
transition: width 1s linear 2s;
/* Safari */
-webkit-transition:width 1s linear 2s;
}