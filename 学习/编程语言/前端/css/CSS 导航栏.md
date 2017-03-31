# CSS 导航栏 #
实例: 导航栏
Home
News
Articles
Forum
Contact
About
导航栏
熟练使用导航栏，对于任何网站都非常重要。
使用CSS你可以转换成好看的导航栏而不是枯燥的HTML菜单。
## 导航栏=链接列表 ##
作为标准的HTML基础一个导航栏是必须的
。在我们的例子中我们将建立一个标准的HTML列表导航栏。
导航条基本上是一个链接列表，所以使用 <ul> 和 <li>元素非常有意义：
实例
<ul>
<li><a href="default.asp">Home</a></li>
<li><a href="news.asp">News</a></li>
<li><a href="contact.asp">Contact</a></li>
<li><a href="about.asp">About</a></li>
</ul>
ul
{
list-style-type:none;
margin:0;
padding:0;
}
例子解析：
list-style-type:none - 移除列表前小标志。一个导航栏并不需要列表标记
移除浏览器的默认设置将边距和填充设置为0
上面的例子中的代码是垂直和水平导航栏使用的标准代码。

## 垂直导航栏 ##
上面的代码，我们只需要 <a>元素的样式，建立一个垂直的导航栏：
实例
    a
    {
    display:block;
    width:60px;
    }
示例说明：
display:block - 显示块元素的链接，让整体变为可点击链接区域（不只是文本），它允许我们指定宽度
width:60px - 块元素默认情况下是最大宽度。我们要指定一个60像素的宽度
提示：查看 完全样式的垂直导航栏的示例.
注意： 请务必指定 <a>元素在垂直导航栏的的宽度。如果省略宽度，IE6可能产生意想不到的效果。

## 水平导航栏 ##
有两种方法创建横向导航栏。使用内联或浮动的列表项。
这两种方法都很好，但如果你想链接到具有相同的大小，你必须使用浮动的方法。
内嵌列表项
建立一个横向导航栏的方法之一是指定
元素， 上述代码是标准的内嵌:
实例
li
{
display:inline;
}
## 浮动列表项 ##
在上面的例子中链接有不同的宽度。
对于所有的链接宽度相等，浮动 <li&gt元素，并指定为 <a>元素的宽度：
实例
li
{
float:left;
}
a
{
display:block;
width:60px;
}
float:left - 使用浮动块元素的幻灯片彼此相邻
display:block - 显示块元素的链接，让整体变为可点击链接区域（不只是文本），它允许我们指定宽度
width:60px - 块元素默认情况下是最大宽度。我们要指定一个60像素的宽度
