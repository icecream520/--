# CSS 按钮 #
## 基本按钮样式 ##
.button {
    background-color: #4CAF50; /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
}
## 按钮颜色 ##
Green Blue Red Gray Black
我们可以使用 background-color 属性来设置按钮颜色:
CSS 实例
.button1 {background-color: #4CAF50;} /* Green */
.button2 {background-color: #008CBA;} /* Blue */
.button3 {background-color: #f44336;} /* Red */ 
.button4 {background-color: #e7e7e7; color: black;} /* Gray */ 
.button5 {background-color: #555555;} /* Black */
## 按钮大小 ##
10px 12px 16px 20px 24px
我们可以使用 font-size 属性来设置按钮大小:
CSS 实例
.button1 {font-size: 10px;}
.button2 {font-size: 12px;}
.button3 {font-size: 16px;}
.button4 {font-size: 20px;}
.button5 {font-size: 24px;}
## 圆角按钮 ##
2px 4px 8px 12px 50%
我们可以使用 border-radius 属性来设置圆角按钮:
CSS 实例
.button1 {border-radius: 2px;}
.button2 {border-radius: 4px;}
.button3 {border-radius: 8px;}
.button4 {border-radius: 12px;}
.button5 {border-radius: 50%;}
## 按钮边框颜色 ##
绿 蓝 红 灰 黑
我们可以使用 border 属性设置按钮边框颜色:
CSS 实例
.button1 {
    background-color: white;
    color: black;
    border: 2px solid #4CAF50; /* Green */
}
...
## 鼠标悬停按钮 ##
绿 蓝 红 灰 黑 
绿 蓝 红 灰 黑
我们可以使用 :hover 选择器来修改鼠标悬停在按钮上的样式。
提示: 我们可以使用 transition-duration 属性来设置 "hover" 效果的速度:
CSS 实例
.button {
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
}

.button:hover {
    background-color: #4CAF50; /* Green */
    color: white;
}
...
## 按钮阴影 ##
阴影按钮 鼠标悬停后显示阴影
我们可以使用 box-shadow 属性来为按钮添加阴影:
CSS 实例
.button1 {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
}

.button2:hover {
    box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}
## 禁用按钮 ##
正常按钮 禁用按钮
我们可以使用 opacity 属性为按钮添加透明度 (看起来类似 "disabled" 属性效果)。
提示: 我么可以添加 cursor 属性并设置为 "not-allowed" 来设置一个禁用的图片:
CSS 实例
.disabled {
    opacity: 0.6;
    cursor: not-allowed;
}
//通过button发现class可以有两个,都可以点的，可以
## 按钮宽度 ##
250px
50% 100%
默认情况下，按钮的大小有按钮上的文本内容决定( 根据文本内容匹配长度 )。 我们可以使用 width 属性来设置按钮的宽度:
提示: 如果要设置固定宽度可以使用像素 (px) 为单位，如果要设置响应式的按钮可以设置为百分比。
CSS 实例
.button1 {width: 250px;}
.button2 {width: 50%;}
.button3 {width: 100%;}
## 按钮组 ##
ButtonButtonButtonButton

移除外边距并添加 float:left 来设置按钮组:
CSS 实例
.button {
    float: left;
}
<p style="clear:both"><br>记住要清除浮动，否则下一个 p 元素的按钮也会显示在同一行。</p>
//清除浮动，达到下一行
## 带边框按钮组 ##
ButtonButtonButtonButton

我们可以使用 border 属性来设置带边框的按钮组:
CSS 实例
.button {
    float: left;
    border: 1px solid green
}
## 按钮动画 ##
CSS 实例
鼠标移动到按钮上后添加箭头标记:
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<style>
.button {
  display: inline-block;
  border-radius: 4px;
  background-color: #f4511e;
  border: none;
  color: #FFFFFF;
  text-align: center;
  font-size: 28px;
  padding: 20px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}

.button span {
  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.button span:after {
  content: '»';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;
}

.button:hover span {
  padding-right: 25px;
}

.button:hover span:after {
  opacity: 1;
  right: 0;
}
</style>
</head>
<body>

<h2>按钮动画</h2>

<button class="button" style="vertical-align:middle"><span>Hover </span></button>

</body>
</html>
CSS 实例
点击时添加 "波纹" 效果:
Click

尝试一下 »
CSS 实例
点击时添加 "压下" 效果: