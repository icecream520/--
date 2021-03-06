# CSS 伪类(Pseudo-classes) #
CSS伪类是用来添加一些选择器的特殊效果。
语法
伪类的语法：
selector:pseudo-class {property:value;}
CSS类也可以使用伪类：
selector.class:pseudo-class {property:value;}
## anchor伪类 ##
在支持 CSS 的浏览器中，链接的不同状态都可以以不同的方式显示
实例
a:link {color:#FF0000;} /* 未访问的链接 */
a:visited {color:#00FF00;} /* 已访问的链接 */
a:hover {color:#FF00FF;} /* 鼠标划过链接 */
a:active {color:#0000FF;} /* 已选中的链接 */
注意： 在CSS定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。
注意： 在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。
注意：伪类的名称不区分大小写。
## 伪类和CSS类 ##
伪类可以与 CSS 类配合使用：
a.red:visited {color:#FF0000;}

<a class="red" href="css-syntax.html">CSS Syntax</a>
如果在上面的例子的链接已被访问，它会显示为红色
### CSS - :first - child伪类 ###
您可以使用 :first-child 伪类来选择元素的第一个子元素
注意：在IE8的之前版本必须声明<!DOCTYPE> ，这样 :first-child 才能生效。
## 匹配第一个 <p> 元素 ##
在下面的例子中，选择器匹配作为任何元素的第一个子元素的 <p> 元素：
实例
<html>
<head>
<style>
p:first-child
{
color:blue;
} 
</style>
</head>

<body>
<p>I am a strong man.</p>
<p>I am a strong man.</p>
</body>
</html>
## 匹配所有<p> 元素中的第一个 <i> 元素 ##
在下面的例子中，选择相匹配的所有<p>元素的第一 <i>元素：
实例
<html>
<head>
<style>
p > i:first-child
{
color:blue;
} 
</style>
</head>

<body>
<p>I am a <i>strong</i> man. I am a <i>strong</i> man.</p>
<p>I am a <i>strong</i> man. I am a <i>strong</i> man.</p>
</body>
</html>
<h2匹配所有作为第一个子元素的<p>元素中的所有<i>元素 ://第一个p中的所有<i>元素
实例
<html>
<head>
<style>
p:first-child i
{
color:blue;
} 
</style>
</head>

<body>
<p>I am a <i>strong</i> man. I am a <i>strong</i> man.</p>
<p>I am a <i>strong</i> man. I am a <i>strong</i> man.</p>
</body>
</html>
## CSS - :lang 伪类 ##
:lang 伪类使你有能力为不同的语言定义特殊的规则
注意：IE8必须声明<!DOCTYPE>才能支持;lang伪类。
在下面的例子中，:lang 类为属性值为 no 的q元素定义引号的类型：
实例
<html>
<head>
<style>
q:lang(no) {quotes: "~" "~";}
</style>
</head>

<body>
<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>
</body>
</html>



<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<style>
input:focus
{
	background-color:yellow;
}
</style>
</head>

<body>
<form action="demo-form.php" method="get">
First name: <input type="text" name="fname" /><br>
Last name: <input type="text" name="lname" /><br>
<input type="submit" value="Submit" />
</form>

<p><b>注意:</b>仅当 !DOCTYPE已经声明时 IE8支持 :focus.</p>

</body>
</html>
## 所有CSS伪类/元素 ##
选择器	示例	示例说明
:checked	input:checked	选择所有选中的表单元素
:disabled	input:disabled	选择所有禁用的表单元素
:empty	p:empty	选择所有没有子元素的p元素
:enabled	input:enabled	选择所有启用的表单元素
:first-of-type	p:first-of-type	选择每个父元素是p元素的第一个p子元素
:in-range	input:in-range	选择元素指定范围内的值
:invalid	input:invalid	选择所有无效的元素
:last-child	p:last-child	选择所有p元素的最后一个子元素
:last-of-type	p:last-of-type	选择每个p元素是其母元素的最后一个p元素
:not(selector)	:not(p)	选择所有p以外的元素
:nth-child(n)	p:nth-child(2)	选择所有p元素的第二个子元素
:nth-last-child(n)	p:nth-last-child(2)	选择所有p元素倒数的第二个子元素
:nth-last-of-type(n)	p:nth-last-of-type(2)	选择所有p元素倒数的第二个为p的子元素
:nth-of-type(n)	p:nth-of-type(2)	选择所有p元素第二个为p的子元素
:only-of-type	p:only-of-type	选择所有仅有一个子元素为p的元素
:only-child	p:only-child	选择所有仅有一个子元素的p元素
:optional	input:optional	选择没有"required"的元素属性
:out-of-range	input:out-of-range	选择指定范围以外的值的元素属性
:read-only	input:read-only	选择只读属性的元素属性
:read-write	input:read-write	选择没有只读属性的元素属性
:required	input:required	选择有"required"属性指定的元素属性
:root	root	选择文档的根元素
:target	#news:target	选择当前活动#news元素(点击URL包含锚的名字)
:valid	input:valid	选择所有有效值的属性
:link	a:link	选择所有未访问链接
:visited	a:visited	选择所有访问过的链接
:active	a:active	选择正在活动链接
:hover	a:hover	把鼠标放在链接上的状态
:focus	input:focus	选择元素输入后具有焦点
:first-letter	p:first-letter	选择每个<p> 元素的第一个字母
:first-line	p:first-line	选择每个<p> 元素的第一行
:first-child	p:first-child	选择器匹配属于任意元素的第一个子元素的 <]p> 元素
:before	p:before	在每个<p>元素之前插入内容
:after	p:after	在每个<p>元素之后插入内容
:lang(language)	p:lang(it)	为<p>元素的lang属性选择一个开始值