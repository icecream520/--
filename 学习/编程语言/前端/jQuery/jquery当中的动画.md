# jQuery当中的动画 #
show(),hide()方法是最基本的动画，hide()方法会将display样式改为none;
$("#id").show(1000);//一秒显示
## fadein()和fadeout() ##
这两个方法只改变元素的不透明度，fadeout()是降低元素的不透明度，直到元素完全消失
## slideUp()和slideDown() ##
这两个方法只会改变元素高度
slideDown()由上至下隐藏，另一个相反 
## 自定义动画 ##
animate(params,speed,callback);
params:一个包含样式属性及值的映射，speed速度参数，callback：在动画完成时执行的函数，可选
多重动画,$(this).animate({left:"500px,height:"2000px"}),300);
如果分开的话就是说，先执行一个再执行另一个。
## 停止动画 ##
stop([clearQueue],[gotoEnd]);
clearQueue:清空未执行完的动画队列
gotoEnd：直接将正在执行的动画跳转到末状态
### 判断元素是否处于动画状态 ###
防止动画积累
if(!$(element).is(":animated")){//判断元素是否处于动画状态

//不处于的时候添加新动画
}