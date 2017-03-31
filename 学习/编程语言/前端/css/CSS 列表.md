## CSS 列表 ##
CSS列表属性作用如下：
设置不同的列表项标记为有序列表
设置不同的列表项标记为无序列表
设置列表项标记为图像

列表
在HTML中，有两种类型的列表：
无序列表 - 列表项标记用特殊图形（如小黑点、小方框等）
有序列表 - 列表项的标记有数字或字母
使用CSS，可以列出进一步的样式，并可用图像作列表项标记。

## 不同的列表项标记 ##
list-style-type属性指定列表项标记的类型是：:
实例
ul.a {list-style-type: circle;}//圆的
ul.b {list-style-type: square;}//方的

ol.c {list-style-type: upper-roman;}//古罗马
ol.d {list-style-type: lower-alpha;}//a,bc

作为列表项标记的图像
要指定列表项标记的图像，使用列表样式图像属性：
实例
ul
{
list-style-image: url('sqpurple.gif');//用图像代替数字等
}
上面的例子在所有浏览器中显示并不相同，IE和Opera显示图像标记比火狐，Chrome和Safari更高一点点。
如果你想在所有的浏览器放置同样的形象标志，就应使用浏览器兼容性解决方案，过程如下
浏览器兼容性解决方案
同样在所有的浏览器，下面的例子会显示的图像标记：
实例
    ul
    {
    list-style-type: none;
    padding: 0px;
    margin: 0px;
    }
    ul li
    {
    background-image: url(sqpurple.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px; 
    padding-left: 14px; 
    }
例子解释：
ul:
设置列表样式类型为没有删除列表项标记
设置填充和边距0px（浏览器兼容性）
ul中所有li:
设置图像的URL，并设置它只显示一次（无重复）
您需要的定位图像位置（左0px和上下5px）
用padding-left属性把文本置于列表中

## 列表 -缩写属性 ##
在单个属性中可以指定所有的列表属性。这就是所谓的缩写属性。
为列表使用缩写属性，列表样式属性设置如下：
实例
ul
{
list-style: square url("sqpurple.gif");
}
如果使用缩写属性值的顺序是：
list-style-type
list-style-position (有关说明，请参见下面的CSS属性表)
list-style-image
如果上述值丢失一个，其余仍在指定的顺序，就没关系。
//所有的类型
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    <style>
    ul.a {
    	list-style-type: circle;
    }
    ul.b {
    	list-style-type: disc;
    }
    ul.c {
    	list-style-type: square;
    }
    ol.d {
    	list-style-type: armenian;
    }
    ol.e {
    	list-style-type: cjk-ideographic;
    }
    ol.f {
    	list-style-type: decimal;
    }
    ol.g {
    	list-style-type: decimal-leading-zero;
    }
    ol.h {
    	list-style-type: georgian;
    }
    ol.i {
    	list-style-type: hebrew;
    }
    ol.j {
    	list-style-type: hiragana;
    }
    ol.k {
    	list-style-type: hiragana-iroha;
    }
    ol.l {
    	list-style-type: katakana;
    }
    ol.m {
    	list-style-type: katagana-iroha;
    }
    ol.n {
    	list-style-type: lower-alpha;
    }
    ol.o {
    	list-style-type: lower-greek;
    }
    ol.p {
    	list-style-type: lower-latin;
    }
    ol.q {
    	list-style-type: lower-roman;
    }
    ol.r {
    	list-style-type: upper-alpha;
    }
    ol.s {
    	list-style-type: upper-latin;
    }
    ol.t {
    	list-style-type: upper-roman;
    }
    ol.u {
    	list-style-type: none;
    }
    ol.v {
    	list-style-type: inherit;
    }
    </style>
    </head>
    
    <body>
    <ul class="a">
      <li>Circle type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ul>
    <ul class="b">
      <li>Disc type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ul>
    <ul class="c">
      <li>Square type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ul>
    <ol class="d">
      <li>Armenian type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="e">
      <li>Cjk-ideographic type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="f">
      <li>Decimal type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="g">
      <li>Decimal-leading-zero type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="h">
      <li>Georgian type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="i">
      <li>Hebrew type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="j">
      <li>Hiragana type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="k">
      <li>Hiragana-iroha type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="l">
      <li>Katakana type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="m">
      <li>Katakana-iroha type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="n">
      <li>Lower-alpha type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="o">
      <li>Lower-greek type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="p">
      <li>Lower-latin type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="q">
      <li>Lower-roman type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="r">
      <li>Upper-alpha type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="s">
      <li>Upper-latin type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="t">
      <li>Upper-roman type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="u">
      <li>None type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    <ol class="v">
      <li>inherit type</li>
      <li>Tea</li>
      <li>Coca Cola</li>
    </ol>
    </body>
    </html>
## 所有的CSS列表属性 ##
属性	描述
list-style	简写属性。用于把所有用于列表的属性设置于一个声明中
list-style-image	将图象设置为列表项标志。
list-style-position	设置列表中列表项标志的位置。
list-style-type	设置列表项标志的类型。