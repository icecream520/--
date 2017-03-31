# CSS 属性 选择器 #
具有特定属性的HTML元素样式
具有特定属性的HTML元素样式不仅仅是class和id。
注意：IE7和IE8需声明!DOCTYPE才支持属性选择器！IE6和更低的版本不支持属性选择器。
## 属性选择器 ##
下面的例子是把包含标题（title）的所有元素变为蓝色：
实例
[title]
{
color:blue;
}
## 属性和值选择器 ##
下面的实例改变了标题title='w3cschool'元素的边框样式:
实例
[title=w3cschool]
{
border:5px solid green;
}
## 属性和值的选择器 - 多值 ##
下面是包含指定值的title属性的元素样式的例子，使用（~）分隔属性和值:
实例
[title~=hello] { color:blue; }//title 包含 hello这个词，注意单个字母不是不行，但是一定要单词，就是说分开的
## 下面是包含指定值的lang属性的元素样式的例子，使用（|）分隔属性和值: ##
实例
[lang|=en] { color:blue; }
//class什么的还是和title一样的
## 表单样式 ##
属性选择器样式无需使用class或id的形式:
实例
//class其实是和title一个量级的，<p><h1>这种事和input一个量级的
input[type="text"]
{
width:150px;
display:block;
margin-bottom:10px;
background-color:yellow;
}
input[type="button"]
{
width:120px;
margin-left:35px;
display:block;
}