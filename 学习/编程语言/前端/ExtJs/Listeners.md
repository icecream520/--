mouseover：鼠标移到相应区域就启动事件
menuhide:目录消失的时候调用
toggle:按钮可以被按下，这个状态调用首先要enabletoggle：true,
蓝色正方体：代表普通的类
粉色正方体：一个单例
cls:类似于重新定义类名，方便下次调用。
## 12种layout ##
[http://http://www.cnblogs.com/mingforyou/p/4119200.html](http://http://www.cnblogs.com/mingforyou/p/4119200.html "Ext12种布局风格介绍")
1.   absolute 顾名思义，在容器内部，根据指定的坐标定位显示 
2.   accordion 这个是最容易记的，手风琴效果
3.   · anchor 这个效果具体还不知道有什么用，就是知道注意一下  
4.   1.容器内的组件要么指定宽度，要么在anchor中同时指定高/宽，  
5.   2.anchor值通常只能为负值(指非百分比值)，正值没有意义，  
6.   3.anchor必须为字符串值
7.   border 将容器分为五个区域:east,south,west,north,center
8.   card 您可以使用卡片布局来创建您自己的自定义向导样式屏幕。布局是一个底部的工具栏标准卡片布局管理器，和开发商必须提供实现向导的业务逻辑导航功能（见basic.js详细代码）。
9.   column 把整个容器看成一列,然后向容器放入子元素时
10.  fit 一个子元素将充满整个容器（如果多个子元素则只有一个元素充满整个容器）
11.  form 是一种专门用于管理表单中输入字段的布局
12.  table 按照普通表格的方法布局子元素，用layoutConfig:{columns:3},//将父容器分成3列
13.  VBOX允许子项目的垂直和横向拉伸的布局，就像大小管理的容器布局
14.  HBox 一个允许子项目的垂直和横向拉伸的布局，非常像列布局，但可以垂直拉伸项目。