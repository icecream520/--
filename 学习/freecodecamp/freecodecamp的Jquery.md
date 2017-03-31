所有jQuery方法都是由$开始的，通常称作为 美元符号，或者简称为bling。

jQuery通过选择器来选择一个元素的，然后操作元素做些改变。

举个例子，要让所有的按钮做弹回效果，只要把这段代码写在document ready function里面就可以了。

$("button").addClass("animated bounce");

我们用 $("button")来选中按钮，然后用.addClass("animated bounce")给按钮加CSS class。

jQuery有一个叫做.css()的方法能让你改变元素的CSS样式。

我们是这样来把颜色改变成蓝色的:

$("#target1").css("color", "blue");

这跟通常的CSS语法有点不同，这里CSS的属性和值是在引号内的，并且用逗号分开。

把你的document ready function清空，

来尝试把target1改变成红色。
当你把按钮设置成不可选以后，这会让按钮变灰并且不能点击。

jQuery有一个.prop()的方法让你来调整元素的属性.

我们是这样来让按钮不可选的:

$("button").prop("disabled", true);

$("button").prop("disabled", true);

jQuery不仅可以改变元素开始标记和结束标记间的文本，甚至可以改变元素标记本身。

jQuery的.html()方法可以添加HTML标签和文字到元素，而元素之前的内容都会被方法的内容所替换掉。

我们是通过em[emphasize]标签来重写和强调标题文本的：

$("h3").html("<em>jQuery Playground</em>");

jQuery 还有一个类似的方法叫.text()，它只能改变文本但不能修改标记。换句话说，这个方法只会把传进来的任何东西(包括标记)当成文本来显示。

任务：强调id为target4按钮里的文本。

jQuery 有一个.remove() 的方法可以移除HTML元素

试着使用.remove()方法来移除页面上的target4元素吧.

现在让我们尝试把元素从一个div里移到另外一个div里。

jQuery有一个appendTo()方法可以把选中的元素加到其他元素中。

比如，你想让target4从我们的从right-well移到left-well，我们可以这样使用:

$("#target4").appendTo("#left-well");

来试着把target2元素从left-well移到right-well中。

除了移动元素，你还可以拷贝元素。简单理解：移动元素就是剪切，拷贝元素就是复制。

jQuery的clone()方法可以拷贝元素。

比如，如果我想把target2从left-well拷贝到right-well，我们可以这样写:

$("#target2").clone().appendTo("#right-well");

你有没有发现两个jQuery方法合在一起使用了？这就叫方法链function chaining，使用起来很方便。

举个例子，h3 元素的父元素是 <div class="container-fluid">，<div class="container-fluid">的父元素是 body。

jQuery有一个方法叫parent()，它允许你访问指定元素的父元素。

举个例子：让left-well 元素的父元素parent()的背景色变成蓝色。

$("#left-well").parent().css("background-color", "blue")


许多HTML元素都有children(子元素)，每个子元素都从父元素那里继承了一些属性。

举个例子，每个HTML元素都是 body 的子元素， 你的 "jQuery Playground" h3 元素是 <div class="container-fluid"> 的子元素。

jQuery有一个方法叫children()，它允许你访问指定元素的子元素。

举个例子：让left-well 元素的子元素children()的文本颜色变成蓝色。


jQuery 用CSS选择器来选取元素，target:nth-child(n) CSS选择器允许你按照索引顺序(从1开始)选择目标元素的所有子元素。

示例：你可以给目标元素的第三个子元素添加bounce class。

$(".target:nth-child(3)").addClass("animated bounce");


$(".target:odd").addClass("animated shake");

记住，jQuery里的索引是从0开始的，也就是说：:odd 选择第2、4、6个元素，因为target#2(索引为1)，target#4(索引为3)，target6(索引为5。

任务：获取class为target且索引为偶数的所有元素，也就是target#1(索引为0)，target#3(索引为2)，target5(索引为4)，并给它们添加class animated 和 shake。

我们让整个body都有淡出效果(fadeOut)： $("body").addClass("animated fadeOut");

让我们做一些更为激动人心的事情，给body添加class animated 和hinge 。

我们让整个body都有淡出效果(fadeOut)： $("body").addClass("animated fadeOut");

让我们做一些更为激动人心的事情，给body添加class animated 和hinge 。