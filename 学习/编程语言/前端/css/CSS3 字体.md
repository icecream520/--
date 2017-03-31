# CSS3 字体 #
With CSS3, web designers are no longer forced to use only web-safe fonts
## CSS3 @font-face 规则 ##
以前CSS3的版本，网页设计师不得不使用用户计算机上已经安装的字体。
使用CSS3，网页设计师可以使用他/她喜欢的任何字体。
当你发现您要使用的字体文件时，只需简单的将字体文件包含在网站中，它会自动下载给需要的用户。
您所选择的字体在新的CSS3版本有关于@font-face规则描述。
您"自己的"的字体是在 CSS3 @font-face 规则中定义的。
使用您需要的字体
在新的 @font-face 规则中，您必须首先定义字体的名称（比如 myFirstFont），然后指向该字体文件。
lamp	提示：URL请使用小写字母的字体，大写字母在IE中会产生意外的结果
如需为 HTML 元素使用字体，请通过 font-family 属性来引用字体的名称 (myFirstFont)：
<style> 
@font-face
{
font-family: myFirstFont;
src: url(sansation_light.woff);
}

div
{
font-family:myFirstFont;
}
</style>

## 使用粗体文本 ##
您必须添加另一个包含粗体文字的@font-face规则：
OperaSafariChromeFirefoxInternet Explorer
实例
@font-face
{
font-family: myFirstFont;
src: url(sansation_bold.woff);
font-weight:bold;
}
该文件"Sansation_Bold.ttf"是另一种字体文件，包含Sansation字体的粗体字。
浏览器使用这一文本的字体系列"myFirstFont"时应该呈现为粗体。
这样你就可以有许多相同的字体@font-face的规则。
## CSS3 字体描述 ##
下表列出了所有的字体描述和里面的@font-face规则定义：
描述符	值	描述
font-family	name	必需。规定字体的名称。
src	URL	必需。定义字体文件的 URL。
font-stretch	
normal
condensed
ultra-condensed
extra-condensed
semi-condensed
expanded
semi-expanded
extra-expanded
ultra-expanded
可选。定义如何拉伸字体。默认是 "normal"。
font-style	
normal
italic
oblique
可选。定义字体的样式。默认是 "normal"。
font-weight	
normal
bold
100
200
300
400
500
600
700
800
900
可选。定义字体的粗细。默认是 "normal"。
unicode-range	unicode-range	可选。定义字体支持的 UNICODE 字符范围。默认是 "U+0-10FFFF"。