Text Color
颜色属性被用来设置文字的颜色。
颜色是通过CSS最经常的指定：
十六进制值 - 如"＃FF0000"
一个RGB值 - "RGB（255,0,0）"
颜色的名称 - 如"红"
参阅 CSS 颜色值 查看完整的颜色值。
一个网页的背景颜色是指在主体内的选择：
实例
body {color:blue;}
h1 {color:#00ff00;}
h2 {color:rgb(255,0,0);}
<p></p> 定义段落的标记 设置属性p{}
<p class="da"></p> 设置属性p.class{}
## 文本的对齐方式 ##
文本排列属性是用来设置文本的水平对齐方式。
文本可居中或对齐到左或右,两端对齐.
当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。
实例
h1 {text-align:center;}
p.date {text-align:right;}
p.main {text-align:justify;}
## 文本修饰 ##
text-decoration 属性用来设置或删除文本的装饰。
从设计的角度看 text-decoration属性主要是用来删除链接的下划线：
实例
a {text-decoration:none;}
也可以这样装饰文字：
实例
h1 {text-decoration:overline;}
h2 {text-decoration:line-through;}
h3 {text-decoration:underline;}

## 文本转换 ##
文本转换属性是用来指定在一个文本中的大写和小写字母。
可用于所有字句变成大写或小写字母，或每个单词的首字母大写。
实例
p.uppercase {text-transform:uppercase;}//全部转换为小写
p.lowercase {text-transform:lowercase;}//全部转换为大写
p.capitalize {text-transform:capitalize;}//所有文字的第一个字母转换为大写
## 文本缩进 ##
文本缩进属性是用来指定文本的第一行的缩进。
实例
p {text-indent:50px;}

## 所有CSS文本属性。 ##
属性	描述
color	设置文本颜色
direction	设置文本方向。 div.ex1 {direction:rtl;},right-to-left
letter-spacing	设置字符间距
line-height	设置行高
text-align	对齐元素中的文本
text-decoration	向文本添加修饰 
text-indent	缩进元素中文本的首行
text-shadow	设置文本阴影 h1 {text-shadow:2px 2px #FF0000;} 第一个像素是相对原位置往后，第二个是下
text-transform	控制元素中的字母
unicode-bidi	设置或返回文本是否被重写 
vertical-align	设置元素的垂直对齐 {vertical-align:text-top;} {vertical-align:text-bottom;}//意识是设置图像在文字上方呢，下方呢这种
white-space	设置元素中空白的处理方式 white-space:nowrap;//禁用文字环绕意思是呈现为一行
word-spacing	设置字间距