# MORE ON STYLE #
You'll appreciate the priorities of style rules//明个种类规则的优先级
## STYLE PROPERTIES WE WILL LOOK AT ##
Pseudo-classes link
               visited
               hover
               active
               empty
anchor伪类
在支持 CSS 的浏览器中，链接的不同状态都可以以不同的方式显示

实例
a:link {color:#FF0000;} /* 未访问的链接 */
a:visited {color:#00FF00;} /* 已访问的链接 */
a:hover {color:#FF00FF;} /* 鼠标划过链接 */
a:active {color:#0000FF;} /* 已选中的链接 */
注意： 在CSS定义中，a:hover 必须被置于 a:link 和 a:visited 之后，才是有效的。

注意： 在 CSS 定义中，a:active 必须被置于 a:hover 之后，才是有效的。

注意：伪类的名称不区分大小写。
直接定义背景颜色要加上style<li style="backgroun:blue">111</li>
<html>
  <head>
    <style>
     li {background:yellow}
    </style>
  </head>
  <body>
   <ul>
    <li>One</li>
    <li>Two</li>
    <li style="background:purple">Three</li>
    <li>Four</li>
   </ul>
  </body>
</html>
## CONTEXT CONTROL ##
You can apply a style rule to a specific context
   ul li {color: red}
Here the style rule is applied to all li
that are inside a ul
<html>
    <head>
        <style>
            ul li {background:yellow}
        </style>
    </head>
    <body>
        <ul>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
            <li>Four</li>
        </ul>
        <ol>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
            <li>Four</li>
        </ol>
    </body>
</html>
## PSEUDO-CLASSES ##
Pseudo-classes are classes with some kind of 'intelligence'
h1:hover {color: red}
When the mouse moves over any h1
the text temporarily changes to red//鼠标移到H1时文本临时改为红色
  link means a link
  visited means a link that has been visited
  active means a link that is currently being followed
  empty means an empty element
a:link {color: red}
a:visited {color: red}
a:active {color: red}
p:empty {color: red}
<html>
    <head>
        <style>
            a:link {background:yellow}
            a:visited {background:pink}
            a:hover {background:lightgreen}
            a:active {background:purple}
            li:empty {background:brown}
        </style>
    </head>
    <body>
        <a href="http://www.google.com">Google</a>
        <a href="http://www.cnn.com">CNN</a>
        <a href="http://www.twitter.com">Twitter</a>
        <a href="http://www.facebook.com">Facebook</a>
        <ol>
            <li>One</li>
            <li>Two</li>
            <li>Three</li>
            <li></li>
        </ol>
    </body>
</html>
<html>
    <head>
	<!--1111-->
        <style>
            a:link {background:yellow}
            a:visited {background:pink}
            a:hover {background:lightgreen}
            a:active {background:purple}
            li:empty {background:brown}
        </style>
    </head>
    <body>
        <a href="http://www.google.com">Google</a>
        <a href="http://www.cnn.com">CNN</a>
        <a href="http://www.twitter.com">Twitter</a>
        <a href="http://www.facebook.com">Facebook</a>
        <ol>
           <!-- <li>One</li>
            <li>Two</li>
            <li>Three</li>
            <li></li>-->
			one<br>
			two<br>
			three<br>

        </ol>
    </body>
</html>

<ol></ol>有序排序 <ul>无序排序</ul> <！==>尴尬只有这个注释<-->
<li> 标签定义列表项目。
<li> 标签可用在有序列表 (<ol>) 和无序列表 (<ul>) 中。
如果没有<li>的话那么就没有行数，浏览器识别为这是一句，没有1,2,3
