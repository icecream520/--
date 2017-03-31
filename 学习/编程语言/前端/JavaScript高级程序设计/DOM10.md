# 节点层次 #
## Element ##
Element类型:用于表现XML和HTML元素,提供了对元素签名.子节点及特性访问
特征：
nodeType的值为1;
nodeName的值为元素的标签名;
nodeValue的值为null;
parentNode可能Document或Element;
var div = document.getElementById("myDiv");
在HTML中标签名始终都以全部大写表示，而在XML中标签名始终会与源代码中的保存一致。最好比较的时候将标签名大小写转换下
if(element.tagName.toLowerCase()=="div")//适用于任何文档
{
}
## HTML元素 ##
id 元素在文档中的唯一标识
title 元素的附件信息,一般通过工具提示条显示出来
lang 元素内容的语言代码,很少使用
dir 语言方向 ltr rtl
className 与元素的class特性对应,元素知道的css类
就是通过.语法得到class名
### 取得特性 ###
操作特性的DOM方法主要有三个 getAttribute(),setAttribute(),removeAttribute();