console.log("")//简单的日志
首先就是说各种输入输出最好放在父元素内部没然后移动父元素来确定位置
absolute：absolute 元素将会脱离正常的文档流，所以 其周围的元素将会忽略它的存在。如同 absolute 元素的 display 属性被设为了 none 一样。此时，我们可以使用 top,bottom,left,right 等属性对 absolute 元素进行绝对定位。一般情况下定义两个属性，top 或 bottom,left 或 right。
元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定，显示层级通过z-index控制。

static：静态定位。如果你没有设置position属性，那么缺省就是static。top，left，bottom，right等属性，在static的情况下是无效的，要使用这些属性，必须把position设置为其他三个值之一。

列表一开始是纵向排列的，通过设置float:left;使其横向排列
margin-left:20px; //设置其与周围的间距
li 列表元素设置字体颜色只需要设置其color属性就Ok了
text-indent:-9999px 使里面的文字消失不见
cursor:pointer; 鼠标移到到上面的时候形状改变为一只手
一个图像你放在界面上，然后你可以通过{ background-position:0px 0px; }来确定你的那个图像
控制列的个数通过<ul><ul></ul></ul>即显示两页
dl 自定义的list样式 dt 列表上部分 dd 列表下部分
display:inline-block；将ul成为一个块状线.padding：4px 是可以空格什么的，可以设置左右
设置虚线
刚刚犯的错的是因为float:left 然后设置的是第二个，然后他就变成第一个了，然后他就炸了，我设置第二个宽度，应该一个全部设置一个的，他先看前面的宽度，然后发现各有各的宽度，后面的设置没用吗，
列表设置显示display:inline-block;是针对li的
margin-left，这种事间距
opacity:0.7;
	background-color:#000000; //设置透明度还有背景透明的
然后很狡诈的是,margin是border与border之间的距离，就是外边距，默认0px则差不多有5px的间距，要负的才行
大的图片要注意，添加alt="",使其图片没有加载出来也有文字
relative 相对位置，你移动了位置也变，那么他也会变化
fixed 相对浏览器进行定位
float-right 的时候你要先确定这个框架的大小，不然是没有办法来让你right的因为一共就那么大，它怎么靠右
padding 是内部的间距， border 是外部间距