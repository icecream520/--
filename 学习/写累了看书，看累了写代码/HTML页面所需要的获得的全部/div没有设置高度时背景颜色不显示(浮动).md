　　在使用div+css进行网页布局时，如果外部div有背景颜色或者边框，而不设置其高度，在IE浏览器下显示正常。但是使用Firefox/opera浏览时却出现最外层Div的背景颜色和边框不起作用的问题。网上查找资料之后主要原因如下：由于在Firefox和opera中：如果里面的DIV是浮动的（float）而母体不会去计算子体float之后的height。而在 IE中支持这种计算，所以IE下正常。

解决方法：
给外部div直接设置高度（不推荐），因为很多时候我们并不知道外部div的高度，我们希望靠里面的div来根据内容自动抻开外边的div，除非你确定的知道外部的div的高度的情况下，所以不建议使用这种方法。
方法一：
在内部每个div后加一个清除浮动（推荐），这样firefox和opera就把里面不当成浮动，会自动计算内部div高度
<div class="outer">
 

<div class="inner1"></div>
  <div class="inner2"></div>
  <div style="clear:both;"></div>
</div>
方法二：
在.outer中加一句overflow:hidden;
overflow 属性规定当内容溢出元素框时发生的事情。如果外层设置了高度，并且高度小于内层占的实际高度，则内层一部分内容会被隐藏。

 

主要想强调的一点是，前面中提到的IE中能够正常显示仅限ie6，在之后的版本中同样也无法设置显示背景颜色。

上面的示例中必须给子元素其中之一添加高度，不然还是无法正常显示背景颜色。实际测试时宽度为0，但父元素的背景颜色可以正常显示。示例代码：

<!doctype html>
<html>
    <head>
        <title>多列浮动</title>
        <meta http-equiv="content-type" content="text/html" charset="utf-8"/>
        <style type="text/css" media="screen">
            body{
                margin:0;
                padding:0;
                text-align:center;
            }

            #menu{
                width:800px;
                margin:0 auto;
                text-align:left;
                background:#ccc;
            }
            #menu ul{
                float:left;
                margin:0px;
                padding:0px;
                list-style:none;
            }
            #menu ul li{
                float:left;
                width:99px;
                display:block;
                line-height:30px;
                text-align:center;
            }
            #menu .menudiv{
                float:left;
                width:1px;
                height:20px;
                background:#888；
                margin-top:5px;
            }
        </style>
    </head>
    <body>
        <div id="menu">
            <ul>
                <li><a href="#">菜单一</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单二</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单三</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单四</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单五</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单六</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单七</a></li>
                <li class="menudiv"/>
                <li><a href="#">菜单八</a></li>
                <li class="menudiv"/>
            </ul>
        </div>
    </body>
</html>

里面id为menu的元素虽然定义了背景颜色，但是由于子元素都设置了float属性，所以无法正常显示背景颜色。

解决方法一：给menu加上overflow:hidden;

解决方法二：直接在menu内ul外面添加<div style="clear:both;"></div> 就是说添加清除浮动的子元素即可

参考资料：http://lovephpor.blog.51cto.com/1850499/563540