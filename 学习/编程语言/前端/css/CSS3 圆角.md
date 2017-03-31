# CSS3 圆角 #
CSS3 圆角
使用 CSS3 border-radius 属性，你可以给任何元素制作 "圆角"。
## CSS3 border-radius 属性 ##
使用 CSS3 border-radius 属性，你可以给任何元素制作 "圆角"。
以下为三个实例：
1. 指定背景颜色的元素圆角：
2.   <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  #rcorners1 {
      border-radius: 25px;
      background: #8AC007;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  #rcorners2 {
      border-radius: 25px;
      border: 2px solid #8AC007;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  #rcorners3 {
      border-radius: 25px;
      background: url(/images/paper.gif);
      background-position: left top;
      background-repeat: repeat;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  </style>
  </head>
  <body>
  <p> border-radius 属性允许向元素添加圆角。</p>
  <p>指定背景颜色元素的圆角:</p>
  <p id="rcorners1">圆角</p>
  <p>指定边框元素的圆角:</p>
  <p id="rcorners2">圆角</p>
  <p>指定背景图片元素的圆角:</p>
  <p id="rcorners3">圆角</p>
  </body>
  </html>
## CSS3 border-radius - 指定每个圆角 ##
如果你在 border-radius 属性中只指定一个值，那么将生成 4 个 圆角。
但是，如果你要在四个角上一一指定，可以使用以下规则：
四个值: 第一个值为左上角，第二个值为右上角，第三个值为右下角，第四个值为左下角。
三个值: 第一个值为左上角, 第二个值为右上角和左下角，第三个值为右下角
两个值: 第一个值为左上角与右下角，第二个值为右上角与左下角
一个值： 四个圆角值相同
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  #rcorners7 {
      border-radius: 50px/15px;
      background: #8AC007;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  #rcorners8 {
      border-radius: 15px/50px;
      background: #8AC007;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  #rcorners9 {
      border-radius: 50%;
      background: #8AC007;
      padding: 20px;
      width: 200px;
      height: 150px;
  }
  </style>
  </head>
  <body>
  <p>椭圆边框 - border-radius: 50px/15px:</p>
  <p id="rcorners7"></p>
  <p> 椭圆边框 - border-radius: 15px/50px:</p>
  <p id="rcorners8"></p>
  <p>椭圆边框 - border-radius: 50%:</p>
  <p id="rcorners9"></p>
  </body>
  </html>
## CSS3 圆角属性 ##
属性	描述
border-radius	所有四个边角 border-*-*-radius 属性的缩写
border-top-left-radius	定义了左上角的弧度
border-top-right-radius	定义了右上角的弧度
border-bottom-right-radius	定义了右下角的弧度
border-bottom-left-radius	定义了左下角的弧度