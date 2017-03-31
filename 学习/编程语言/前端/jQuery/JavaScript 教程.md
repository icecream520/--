为什么学习 JavaScript?
JavaScript web 开发人员必须学习的 3 门语言中的一门：
HTML 定义了网页的内容
CSS 描述了网页的布局
JavaScript 网页的行为
本教程是关于 JavaScript 及介绍 JavaScript 如何与 HTML 和 CSS 一起工作。
JavaScript 是脚本语言
JavaScript 是一种轻量级的编程语言。
JavaScript 是可插入 HTML 页面的编程代码。
JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行。
JavaScript 很容易学习。
## JavaScript：直接写入 HTML 输出流 ##
实例
document.write("<h1>这是一个标题</h1>");
document.write("<p>这是一个段落。</p>");
## JavaScript：对事件的反应 ##
实例
<button type="button" onclick="alert('欢迎!')">点我!</button>
alert() 函数在 JavaScript 中并不常用，但它对于代码测试非常方便。
onclick 事件只是您即将在本教程中学到的众多事件之一。
## JavaScript：改变 HTML 内容 ##
使用 JavaScript 来处理 HTML 内容是非常强大的功能。
实例
x=document.getElementById("demo")  //查找元素
x.innerHTML="Hello JavaScript";    //改变内容
您会经常看到 document.getElementById("some id")。这个方法是 HTML DOM 中定义的。
DOM (Document Object Model)（文档对象模型）是用于访问 HTML 元素的正式 W3C 标准。
您将在本教程的多个章节中学到有关 HTML DOM 的知识。
## JavaScript：改变 HTML 图像 ##
本例会动态地改变 HTML <image> 的来源（src）：
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
	
<script>
function changeImage()
{
	element=document.getElementById('myimage')
	if (element.src.match("pic_bulbon"))
 	{
  		element.src="/images/pic_bulboff.gif";
  	}
	else
   {
  		element.src="/images/pic_bulbon.gif";
   }
}
</script>
<img id="myimage" onclick="changeImage()"
src="/images/pic_bulboff.gif" width="100" height="180">
<p>点击灯泡就可以打开或关闭这盏灯</p>
	
</body>
</html>
## JavaScript：改变 HTML 样式 ##
改变 HTML 元素的样式，属于改变 HTML 属性的变种。
实例
x=document.getElementById("demo")  //找到元素 
x.style.color="#ff0000";           //改变样式
## JavaScript：验证输入 ##
JavaScript 常用于验证用户的输入。
实例
if isNaN(x) {alert("不是数字")};