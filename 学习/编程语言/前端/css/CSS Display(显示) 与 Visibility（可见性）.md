# CSS Display(显示) 与 Visibility（可见性） #
display属性设置一个元素应如何显示，visibility属性指定一个元素应可见还是隐藏。
隐藏元素 - display:none或visibility:hidden
隐藏一个元素可以通过把display属性设置为"none"，或把visibility属性设置为"hidden"。但是请注意，这两种方法会产生不同的结果。
visibility:hidden可以隐藏某个元素，但隐藏的元素仍需占用与未隐藏之前一样的空间。也就是说，该元素虽然被隐藏了，但仍然会影响布局。
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  h1.hidden {
      visibility: hidden;
      h1.hidden {display:none;}//这个是不占用空间的，而且优先级更高
  }
  </style>
  </head>
  
    <body>
  <h1>这是一个可见标题</h1>
  <h1 class="hidden">这是一个隐藏标题</h1>
  <p>注意, 实例中的隐藏标题仍然占用空间。</p>
  </body>
  </html>
  display:none可以隐藏某个元素，且隐藏的元素不会占用任何空间。也就是说，该元素不但被隐藏了，而且该元素原本占用的空间也会从页面布局中消失。
实例
h1.hidden {display:none;}
## CSS Display - 块和内联元素 ##
CSS Display - 块和内联元素
块元素是一个元素，占用了全部宽度，在前后都是换行符。
块元素的例子：
<h1>
<p>
<div>
内联元素只需要必要的宽度，不强制换行。
内联元素的例子：
<span>
<a>
## 如何改变一个元素显示 ##
可以更改内联元素和块元素，反之亦然，可以使页面看起来是以一种特定的方式组合，并仍然遵循web标准。
下面的示例把列表项显示为内联元素：
实例
li {display:inline;}
  <!DOCTYPE html>
  <html>
  <head>
  <meta charset="utf-8">
  <title>菜鸟教程(runoob.com)</title>
  <style>
  li {
      display: inline;//将所有的元素呈现在一条线上
  }
  </style>
  </head>
  <body>
  <p>链接列表水平显示：</p>
  <ul>
    <li><a href="/html/" target="_blank">HTML</a></li>
    <li><a href="/css/" target="_blank">CSS</a></li>
    <li><a href="/js/" target="_blank">JavaScript</a></li>
    <li><a href="/xml/" target="_blank">XML</a></li>
  </ul>
  </body>
  </html>
 下面的示例把span元素作为块元素：
实例
span {display:block;}//本来这个不是块元素，不会有空格，有些元素是自带空格的，明显<span>是没有的，但是这个操作之后它就有了
注意：变更元素的显示类型看该元素是如何显示，它是什么样的元素。例如：一个内联元素设置为display:block是不允许有它内部的嵌套块元素。

//内联属性和块属性的差别就是中间有无换行，要是内联则<p>1</p><p>2</p>在一起的，但是block则换行
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<style>
table, th, td {
	border: 1px solid black;
}
tr.collapse {
	visibility: collapse;
}
</style>
</head>
<body>
<table>
  <tr>
    <th>Firstname</th>
    <th>Lastname</th>
  </tr>
  <tr>
    <td>Peter</td>
    <td>Griffin</td>
  </tr>
  <tr class="collapse">
    <td>Lois</td>
    <td>Griffin</td>
  </tr>
</table>
<p><b>注意:</b> IE8 及其更早版本需要通过指定 !DOCTYPE 才可以支持 visibility:collapse。</p>
</body>
</html>
//这个例子演示了如何使用表的collapse属性。就是数据消失，但是占有的空间还是有的