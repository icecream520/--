# CSS 图像透明/不透明 #
使用CSS很容易创建透明的图像。
//即鼠标经过的时候图像由透明到不透明
注意：CSS Opacity属性是W3C的CSS3建议的一部分。
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  img {
      opacity: 0.4;
      //初始的时候，透明度设置为0.4
      filter: alpha(opacity=40); /* 适用 IE8 及其更早版本 */
  }
  img:hover {
      opacity: 1.0;
      //然后经过图片的时候就设为1.0了
      filter: alpha(opacity=100); /* 适用 IE8 及其更早版本 */
  }
  </style>
  </head>
  <body>
  <h1>图片透明度</h1>
  <p>opacity 属性通常与 :hover 选择器一起使用，在鼠标移动到图片上后改变图片的透明度：</p>
  <img src="klematis.jpg" width="150" height="113" alt="klematis"> <img src="/images/klematis2.jpg" width="150" height="113" alt="klematis">
  <p><b>注意:</b>在 IE 中必须声明 &lt;!DOCTYPE&gt; 才能保证 :hover 选择器能够有效。</p>
  </body>
  </html>
看看下面的CSS：
img
{
opacity:0.4;
filter:alpha(opacity=40); /* For IE8 and earlier */
}
IE9，Firefox，Chrome，Opera，和Safari浏览器使用透明度属性可以将图像变的不透明。 Opacity属性值从0.0 - 1.0。值越小，使得元素更加透明。
IE8和早期版本使用滤镜：alpha（opacity= x）。 x可以采取的值是从0 - 100。较低的值，使得元素更加透明。
CSS样式：
img
{
opacity:0.4;
filter:alpha(opacity=40); /* For IE8 and earlier */
}
img:hover
{
opacity:1.0;
filter:alpha(opacity=100); /* For IE8 and earlier */
}
第一个CSS块是和例1中的代码类似。此外，我们还增加了当用户将鼠标悬停在其中一个图像上时发生什么。在这种情况下，当用户将鼠标悬停在图像上时，我们希望图片是清晰的。
此CSS是：opacity=1.
IE8和更早版本使用： filter:alpha(opacity=100).
当鼠标指针远离图像时，图像将重新具有透明度。
## 实例3 - 透明的盒子中的文字 ##
  <html>
  <head>
  <style>
  div.background {
      width: 500px;
      height: 250px;
      background: url(klematis.jpg) repeat;
      //他图片重复
      border: 2px solid black;
      //线宽还有黑色实线
  }
  div.transbox {
      width: 400px;
      height: 180px;
      margin: 30px 50px;
      background-color: #ffffff;
      border: 1px solid black;
      opacity: 0.6;
      filter: alpha(opacity=60); /* For IE8 and earlier */
  }
  div.transbox p {
      margin: 30px 40px;
      //外边框也有调整
      font-weight: bold;
      //这个class 里面的p加粗了
      color: #000000;
  }
  </style>
  </head>
  
  <body>
  <div class="background">
    <div class="transbox">
      <p>This is some text that is placed in the transparent box.
        This is some text that is placed in the transparent box.
        This is some text that is placed in the transparent box.
        This is some text that is placed in the transparent box.
        This is some text that is placed in the transparent box. </p>
    </div>
  </div>
  </body>
  </html>