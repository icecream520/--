http://blog.csdn.net/yisuowushinian/article/details/52728374
4.传递参数的解决方案
在开发过程曾经遇到过这样的问题：

很多个页面，比如说a-z。当我在a页面的时候，浏览器中的url会带有某些参数，当我在做完一系列的操作到达z页面。
某天有个需求，用户在页面a的时候会带上一个参数，决定用户在z页面做完操作后页面最终跳向哪里。那么这个参数该怎么传递到z页面呢？

第一种解决方案：

从a页面到z页面跳转的过程中，通过 GET 的方式在url中带上这个参数；

这种方案是比较常规，也是比较不错的解决方案。但是需要在页面中的逻辑跳都加上需要的参数。这样工作量比较大，而且容易出现遗漏。不建议使用。

第二种解决方案：

使用html5新特性sessionStorage来解决问题。在a页面的时候，把新添加的需要传给z页面的参数放在sessionStorage中。在z页面直接从sessionStorage中取需要获取的参数值，然后决定页面最终的跳转。

这样解决问题不仅减少了很大的工作量，也解决了工作量大会遗漏的问题。

sessionStorage的优点：

因为数据是存储在内存中，当会话结束，页面关闭以后这些数据就会被销毁。
html5移动端存储的一些坑：

当然在移动端浏览器中使用localStorage和sessionStorage是没有任何问题的。但是在安卓webview中却出现了localStorage无法向移动的磁盘写数据的问题。最后通过网络搜索发现。在安卓上webview是默认不开启localStorage想磁盘写文件的权限的。所以如果需要使用localStorage的同学需要找客户端支持。详细信息如下：

pc端js生成二维码
做过一个JavaScript生成二维码的需求。当时调研了两个方案：

使用qrcodejs
使用jQuery.qrcide

关于锚点 锚点就是说是页面内部本身的链接 通过 <a href="#锚点"> <a name="锚点">
然后表格的话 格式是
<table>
 <caption></caption>
 <tr>
 <th></th>
</tr>
<tr>
<td></td>
</tr>
</table>
首先caption为表头,然后每一行都需要tr格式 然后注意有个很重要的属性 rowspan="num" 是这个td占了几行

然后注意可以使用<frameset>来代替<body>前面这个是为了完成布局的，你要是没用其他框架的话这个可以完成布局
然后子窗口标签为<frame><>frame>,然后<frameset>里面还可以嵌套这个，就是说先划分上下，然后在这里面再划分左右
<form>表单我们已经知道是提交信息的了，同时也要告诉其处理脚本程序的位置，提交表单的方法，要是不说吗，默认是get
<form>中必须添加action属性，为处理程序的程序名地址,空也必须定义为action="no",<form action="login.php" method="post">
<input type="password">则输入的内容以*隐藏
复选框和单选框都只有在选中时，数据才能被提交到服务器端，他们的名称必须相同才会排斥
多行文本域，没有输入字符长度限制，<form><textarea>
菜单下拉列表域： <select>
<option>
</select>