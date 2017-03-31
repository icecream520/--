e是事件，在firefox中只能在事件现场使用window.event，所以只有把event传给函数使用。为了兼容FF和其它浏览器，一般会在函数里重新给e赋值：
e = window.event || e;
也就是说，如果window.event存在，则该浏览器支持直接使用window.event，否在就是不支持，不支持就使用传进来的e。 

如下代码：
<SCRIPT LANGUAGE="JavaScript">
<!--
window.onload = function(e){
//alert(window.event.type) // IE时调用，非IE注释掉否则报错
alert(e.type); // FF时调用，非FF注释掉否则报错
// 由于这里的事件是window.onload ，所以打印type两个都会显示”load“。
}
//-->
</SCRIPT>
## 局部变量定义 ##
var $content = $(this).next();
把这步的操作全部定义为一个变量
## bind 绑定事件 ##
bind(type [, data] , fn)；
第一参数为事件类型双击，单机什么的
第二个参数为可选参数，属性值传递
第三个参数 用来绑定处理函数的
例：$("#panel h5.head").bind("mouseover",function(){


}).bind("mouseout",function(){


})
调试的时候所有的w3w
## 合成事件 ##
hover(enter,leave)

bind().bind();

toggle(fn1,fn2);

$("#panel h5.head").toggle(function(){
    $(this).next().toggle();      

},function(){
   $(this).next().toggle();
}
);
//toggle()方法切换元素的可见状态，如果元素是可见的，单击切换为隐藏，隐藏单击后为可见
## 停止冒泡事件 ##
event.stopPropagation();

## 阻止默认行为 ##
阻止元素的默认行为，例如点击链接之后的跳转等，表单提交等
event.preventDefault();

同时对象停止冒泡和默认行为，可以在处理事件函数中返回false。
return false;