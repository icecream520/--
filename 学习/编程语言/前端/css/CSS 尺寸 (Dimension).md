# CSS 尺寸 (Dimension) #
CSS 尺寸 (Dimension) 属性允许你控制元素的高度和宽度。同样，它允许你增加行间距。
所有CSS 尺寸 (Dimension)属性
属性	描述
height	设置元素的高度。
line-height	设置行高。
max-height	设置元素的最大高度。
max-width	设置元素的最大宽度。//设置最大值到挺有用的
min-height	设置元素的最小高度。
min-width	设置元素的最小宽度。//就是说设置每个宽最小值，最大值则不固定
width	设置元素的宽度。
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  img.normal {
    height: auto;
  }
  img.big {
    height: 120px;
  }
  p.ex {
    height: 100px;
    width: 100px;
  }
  </style>
  </head>
  
  <body>
  <img class="normal" src="logocss.gif" width="95" height="84" /><br>
  <img class="big" src="logocss.gif" width="95" height="84" />
  <p class="ex">这个段落的高和宽是 100px.</p>
  <p>这是段落中的一些文本。这是段落中的一些文本。
  这是段落中的一些文本。这是段落中的一些文本。
  这是段落中的一些文本。这是段落中的一些文本.</p>
  </body>
  </html>