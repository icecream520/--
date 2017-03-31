什么是 CSS Float（浮动）？
CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。
Float（浮动），往往是用于图像，但它在布局时一样非常有用。
## 元素怎样浮动 ##
元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。
一个浮动元素会尽量向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。
浮动元素之后的元素将围绕它。
浮动元素之前的元素将不会受到影响。
如果图像是右浮动，下面的文本流将环绕在它左边：
实例
img
{
float:right;
}
## 彼此相邻的浮动元素 ##
如果你把几个浮动的元素放到一起，如果有空间的话，它们将彼此相邻。
在这里，我们对图片廊使用 float 属性：
实例
.thumbnail 
{
float:left;
width:110px;
height:90px;
margin:5px;
}
## 清除浮动 - 使用 clear ##
元素浮动之后，周围的元素会重新排列，为了避免这种情况，使用 clear 属性。
clear 属性指定元素两侧不能出现浮动元素。
使用 clear 属性往文本中添加图片廊：
实例
.text_line
{
clear:both;
}
CSS 中所有的浮动属性
"CSS" 列中的数字表示不同的 CSS 版本（CSS1 或 CSS2）定义了该属性。
属性	描述	值	CSS
clear	指定不允许元素周围有浮动元素。	left
right
both
none
inherit	1
float	指定一个盒子（元素）是否可以浮动。	left
right
none
inherit

### 创建一个没有表格的网页使用 float 创建一个网页页眉、页脚、左边的内容和主要内容。 ###
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  div.container {
      width: 100%;
      margin: 0px;
      border: 1px solid gray;
      line-height: 150%;
  }
  div.header, div.footer {
      padding: 0.5em;
      color: white;
      background-color: gray;
      clear: left;
  }
  h1.header {
      padding: 0;
      margin: 0;
  }
  div.left {
      float: left;
      width: 160px;
      margin: 0;
      padding: 1em;
  }
  div.content {
      margin-left: 190px;
      border-left: 1px solid gray;
      padding: 1em;
  }
  </style>
  </head>
  <body>
  <div class="container">
    <div class="header">
      <h1 class="header">w3cschool.cc</h1>
    </div>
    <div class="left">
      <p>"Never increase, beyond what is necessary, the number of entities required to explain anything." William of Ockham (1285-1349)</p>
    </div>
    <div class="content">
      <h2>Free Web Building Tutorials</h2>
      <p>At w3cschool you will find all the Web-building tutorials you need,
        from basic HTML and XHTML to advanced XML, XSL, Multimedia and WAP.</p>
      <p>w3cschool - The Largest Web Developers Site On The Net!</p>
    </div>
    <div class="footer">Copyright 1999-2005 by Refsnes Data.</div>
  </div>
  </body>
  </html>