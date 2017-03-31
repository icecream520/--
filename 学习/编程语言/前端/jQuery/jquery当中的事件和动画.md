# 移除事件 #
一个元素可以添加多个点击事件，同时相应
 $("#test").bind("click",function(){

}).bind("click",function(){

})
## 移除按钮元素上以前注册的事件 ##
unbind([type],[data]);
第一个参数时事件类型，第二个参数是将要移除的函数
(1)如果没有参数，则删除所有的绑定的事件。
$("#id").unbind("click");
## 删除特定事件 ##
$("#id").bind("click",bth=function(){

});

$("#id2").unbind("click",bth);
### 点击一次后瞬间删除事件 ###
$("#id").one("click",bth=function(){

})
## 模拟操作 ##
$("#id").trigger("click");
模拟点击事件，完成一次点击操作，所有的click都会有一次模拟点击
trigger操作会执行浏览器默认操作。得到焦点
## 其他用法 ##
可以一次绑定多个事件类型,$("div").bind("mouseover mouseout",function(){


})
## 添加事件命名空间 ##
$("div").bind("click.class",bth=function(){


})

$("button").bind("click",function(){
$("btn").unbind(".class");
})