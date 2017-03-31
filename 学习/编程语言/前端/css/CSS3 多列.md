# CSS3 多列 #
CSS3 可以将文本内容设计成像报纸一样的多列布局，如下实例:
菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程(www.runoob.com)提供了最全的编程技术基础教程, 介绍了HTML、CSS、Javascript、Python，Java，Ruby，C，PHP , MySQL等各种编程语言的基础知识。 同时本站中也提供了大量的在线实例，通过实例，您可以更好的学习编程。
## CSS3 多列属性 ##
本章节我们将学习以下几个 CSS3 的多列属性:
column-count
column-gap
column-rule-style
column-rule-width
column-rule-color
column-rule
column-span
column-width
## CSS3 创建多列 ##
column-count 属性指定了需要分割的列数。
以下实例将 <div> 元素中的文本分为 3 列：
实例
div {
    -webkit-column-count: 3; /* Chrome, Safari, Opera */
    -moz-column-count: 3; /* Firefox */
    column-count: 3;
}
## CSS3 多列中列与列间的间隙 ##
column-gap 属性指定了列与列间的间隙。
以下实例指定了列与列间的间隙为 40 像素：
实例
div {
    -webkit-column-gap: 40px; /* Chrome, Safari, Opera */
    -moz-column-gap: 40px; /* Firefox */
    column-gap: 40px;
}
## CSS3 列边框 ##
column-rule-style 属性指定了列与列间的边框样式：
实例
div {
    -webkit-column-rule-style: solid; /* Chrome, Safari, Opera */
    -moz-column-rule-style: solid; /* Firefox */
    column-rule-style: solid;
}
column-rule-width 属性指定了两列的边框厚度:
实例
div {
    -webkit-column-rule-width: 1px; /* Chrome, Safari, Opera */
    -moz-column-rule-width: 1px; /* Firefox */
    column-rule-width: 1px;
}
olumn-rule-color 属性指定了两列的边框颜色：
实例
div {
    -webkit-column-rule-color: lightblue; /* Chrome, Safari, Opera */
    -moz-column-rule-color: lightblue; /* Firefox */
    column-rule-color: lightblue;
}
column-rule 属性是 column-rule-* 所有属性的简写。
以下实例设置了列直接的边框的厚度，样式及颜色：
实例
div {
    -webkit-column-rule: 1px solid lightblue; /* Chrome, Safari, Opera */
    -moz-column-rule: 1px solid lightblue; /* Firefox */
    column-rule: 1px solid lightblue;
}
指定元素跨越多少列
以下实例指定 <h2> 元素跨越所有列：
实例
h2 {
    -webkit-column-span: all; /* Chrome, Safari, Opera */
    column-span: all;
}
指定列的宽度
column-width 属性指定了列的宽度。
实例
div {
    -webkit-column-width: 100px; /* Chrome, Safari, Opera */
    column-width: 100px;
}
## CSS3 多列属性 ##
下表列出了所有 CSS3 的多列属性：
属性	描述
column-count	指定元素应该被分割的列数。
column-fill	指定如何填充列
column-gap	指定列与列之间的间隙
column-rule	所有 column-rule-* 属性的简写
column-rule-color	指定两列间边框的颜色
column-rule-style	指定两列间边框的样式
column-rule-width	指定两列间边框的厚度
column-span	指定元素要跨越多少列
column-width	指定列的宽度
columns	设置 column-width 和 column-count 的简写