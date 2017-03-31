# BOM #
bom的核心对象是window,它表示浏览器的一个实例。
定义全局变量

var newValue = oldValue;
//这里不会抛出错误，因为这是一次属性查询。
var newValue = windows.oldValue;

moveTo()新位置的x和y坐标值。moveBy()接收的是在水平和垂直方向上移动的像素数。

resizeTo()接收浏览器窗口的新宽度和新高度,resizeBy()接收新窗口与原窗口的高度之差。

## 导航和打开窗口 ##
使用window.open()方法可以导航到一个特定URL,也可以打开一个新的浏览器窗口。4个参数：要加载的URL。窗口目标.一个特性字符串以及一个新页面是否取代浏览器历史记录中单枪加载页面的bool值。
window.open("http://www.baidu.com/","topFrame"); 
就如同用户单机了href属性。


## 间歇调用超时调用 ##
js是单线程语言,但他允许通过设置超时值和间歇时间值来调度代码在特定的时刻执行，
前者在指定的时间过后执行代码，而后者则是每隔指定的时间就执行一次代码。
超时调用:window对象的setTimeout();
调用setTimeout()之后，该方法会返回一个数值ID。这个超时调用ID是计划执行代码的唯一标识符，可以通过它来取消超时调用。要取消超时调用
调用cleraTimeout()方法,并将超时调用ID作为参数传递给它。

间歇调用:setInterval(),同样也会返回一个间歇调用ID,可以用来取消间歇调用,clearInterval(),并传入id。
alert(),confirm(),prompt(),通过这几个方法打开的对话框都是同步和模态的，显示这些对话框的时候代码会停止执行，而关掉这些对话框后代码又会恢复执行。

confirm()确认取消。
prompt()输入内容。ok输入的内容不为Null.

### location ###
location对象即是window对象，也是document对象属性。
location对象的用处1.保存着当前文档的信息。2.它将URL解析为独立的片段。
与位置有关的最后一个方法是reload(),作用是重新加载当前显示的页面,如果调用reload()时不传递任何参数,页面就会以最有效的方式重新加载,就是说页面没有改变过则从浏览器缓存中重新加载，如果强制从服务器重新加载则需要像下面这样为该方法传递参数true。

## navigator对象 ##
识别客户端浏览器的事实标准

## 检测插件 ##
可以使用plugins数组,
name:插件名字
description：插件的描述
filename:插件的文件名
lentgth:插件的MIME类型数量
### 小结 ###
BOM以windows对象为依托，表示浏览器窗口及页面可见区域，