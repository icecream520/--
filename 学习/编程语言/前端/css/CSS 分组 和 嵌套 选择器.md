CSS 分组 和 嵌套 选择器
Grouping Selectors
在样式表中有很多具有相同样式的元素。
h1
{
color:green;
}
h2
{
color:green;
}
p
{
color:green;
}
为了尽量减少代码，你可以使用分组选择器。
每个选择器用逗号分隔.
在下面的例子中，我们对以上代码使用分组选择器：
实例
h1,h2,p
{
color:green;
}
## 嵌套选择器 ##
它可能适用于选择器内部的选择器的样式。
在下面的例子设置了三个样式：
为所有p元素指定一个样式
为所有class="marked"的元素指定一个样式
为所有class="marked"元素内的p元素指定一个样式
实例
p
{
color:blue;
text-align:center;
}
.marked
{
background-color:red;
}
.marked p//类似于一个大的class类名为"marked"，然后里面可能会有p元素，然后其颜色改变为
{
color:white;
}