# HTML5 拖放（Drag 和 Drop） #
拖放（Drag 和 drop）是 HTML5 标准的组成部分。

将w3cschool图标拖动到矩形框中。
拖放
拖放是一种常见的特性，即抓取对象以后拖到另一个位置。
在 HTML5 中，拖放是标准的一部分，任何元素都能够拖放。
浏览器支持
Internet ExplorerFirefoxOperaGoogle ChromeSafari
Internet Explorer 9+, Firefox, Opera, Chrome, 和 Safari 支持拖动。
注意:Safari 5.1.2不支持拖动.
## HTML5 拖放实例 ##
下面的例子是一个简单的拖放实例
<!DOCTYPE HTML>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<style type="text/css">
#div1 {width:350px;height:70px;padding:10px;border:1px solid #aaaaaa;}
</style>
<script>
function allowDrop(ev)
{
    ev.preventDefault();
}

function drag(ev)
{
    ev.dataTransfer.setData("Text",ev.target.id);
}

function drop(ev)
{
    ev.preventDefault();
    var data=ev.dataTransfer.getData("Text");
    ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<p>拖动 W3CSchool.cc 图片到矩形框中:</p>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)"></div>
<br>
<img id="drag1" src="/images/logo.png" draggable="true" ondragstart="drag(event)" width="336" height="69">

</body>
</html>
它看上去也许有些复杂，不过我们可以分别研究拖放事件的不同部分。
设置元素为可拖放
首先，为了使元素可拖动，把 draggable 属性设置为 true ：
<img draggable="true">

拖动什么 - ondragstart 和 setData()
然后，规定当元素被拖动时，会发生什么。
在上面的例子中，ondragstart 属性调用了一个函数，drag(event)，它规定了被拖动的数据。
dataTransfer.setData() 方法设置被拖数据的数据类型和值：
function drag(ev)
{
    ev.dataTransfer.setData("Text",ev.target.id);
}
在这个例子中，数据类型是 "Text"，值是可拖动元素的 id ("drag1")。
它看上去也许有些复杂，不过我们可以分别研究拖放事件的不同部分。
设置元素为可拖放
首先，为了使元素可拖动，把 draggable 属性设置为 true ：
<img draggable="true">

拖动什么 - ondragstart 和 setData()
然后，规定当元素被拖动时，会发生什么。
在上面的例子中，ondragstart 属性调用了一个函数，drag(event)，它规定了被拖动的数据。
dataTransfer.setData() 方法设置被拖数据的数据类型和值：
function drag(ev)
{
    ev.dataTransfer.setData("Text",ev.target.id);
}
在这个例子中，数据类型是 "Text"，值是可拖动元素的 id ("drag1")。
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title>
<style type="text/css">
#div1, #div2
{float:left; width:100px; height:35px; margin:10px;padding:10px;border:1px solid #aaaaaa;}
</style>
<script>
function allowDrop(ev)
{
	ev.preventDefault();
}

function drag(ev)
{
	ev.dataTransfer.setData("Text",ev.target.id);
}

function drop(ev)
{
	ev.preventDefault();
	var data=ev.dataTransfer.getData("Text");
	ev.target.appendChild(document.getElementById(data));
}
</script>
</head>
<body>

<div id="div1" ondrop="drop(event)" ondragover="allowDrop(event)">
	<img src="img_w3slogo.gif" draggable="true" ondragstart="drag(event)" id="drag1" width="88" height="31"></div>
<div id="div2" ondrop="drop(event)" ondragover="allowDrop(event)"></div>

</body>
</html>