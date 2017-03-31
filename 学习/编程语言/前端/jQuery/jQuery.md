$是jQuery的一个简写形式$.ajax和jQuery.ajax是等价的
windows.onload 与$(document).ready()第一个要等网页中所有内容加载完毕，另一个等DOM加载完毕，编写个数不同
Ext是可以和jQuery混用的
DOM对象获取：JavaScript方法
var domObj = document.getElementByid("id");//获得DOM对象
var ObjHTML = domObj.innerHTML;//使用JavaScript中的属性————innerHTML
jQuery对象
$("#foo").html();//获取id为foo的元素内的Html代码。.html()是jQuery方法
jQuery和DOM对象方法不能混用
jquer对象命名 var $variable = jquery对象
DOM对象命名 var variable = DOM对象

CSS选择器:层叠样式表，网页结构和表现形式完全分离，对元素添加样式而不改动HTML结构，某个样式用于特定的HTML元素，先找到该元素，在CSS中，执行这一任务的表现规则成为CSS选择器。
CSS获取到元素的代码：.demo{

}
jQuery获取到元素的代码
$(".demo").click(function(){
....

})//获取到这个元素然后给他添加一个点击事件

CSS选择器选择到元素后是添加样式，jQuery是添加行为
$("#tt").css("color","red");//无需判断id'tt'是否存在
这个方法获取的永远是对象，不过网页上有没有此元素，因此不能拿来判断对象是否存在，要用
if($("#tt").length>0){

}或者转化为DOM对象来处理
if($("#tt")[0])
{

}
在网页中每个id只能使用一次，class允许重复使用