# TABLES #
## TABLES ##
HTML tables are a way to get a structured layout
To do this, several different tags work together//HTML是一种有结构的布局要做到这一点，几个不同的标签一起工作
## ELEMENTS WE WILL LOOK AT ##
The structure <table> <thead> <tbody>
The header <th>
The body <tr> <td>
## STYLE PROPERTIES WE WILL LOOK AT ##
Table borders border
Table width width
Table height height
Vertical alignment vertical‐align
Table padding padding
## TABLE STRUCTURE ##//表结构
<table>
   <thead>
     <tr> <th>...</th> <th>...</th> <th>...</th> </tr>
   </thead>
   <tbody>
     <tr> <td>...</td> <td>...</td> <td>...</td> </tr>
     <tr> <td>...</td> <td>...</td> <td>...</td> </tr>
   </tbody>
</table>
<tr> 标签定义 HTML 表格中的行。
tr 元素包含一个或多个 th 或 td 元素。//<tr>行数<th>表的表头，类似此列名字，<td>这一行的内容，距离好像是自动的
## A SIMPLE EXAMPLE ##
<table>
    <thead>
        <tr> 
            <th>Skills</th> 
            <th>Difficulty</th> 
            <th>My Level</th> 
        </tr>
    </thead>
    <tbody>
	 <table>
            <tr> 
                <td>HTML</td> 
                <td>Easy</td> 
                <td>Some</td> 
            </tr>
            <tr> 
                <td>CSS</td> 
                <td>Medium</td> 
                <td>A little</td> 
            </tr>
            <tr> 
                <td>JavaScript</td> 
                <td>Hard</td> 
                <td>Zero</td> 
				<td>GiveUp</td> 
            </tr>
	 </table>
    </tbody>
</table>
## COMMONLY USED STYLE PROPERTIES ##
color for text color
text‐align for horizontal text alignment
border for table borders
width for table width
height for table height
vertical‐align for vertical text alignment
padding for table padding
<html>
    <head> 
        <style>
            table, td, th {border:1px solid black; padding:15px}//1px一像素，1px solid black//一像素的黑色实线边框
            td {color:purple}
        </style> 
    </head>
    <body>
        <table>
            <tr>
                <th>Menu</th>
                <th>Price</th>
            </tr>
            <tr>
                <td>Snail pizza</td>
                <td>$15</td>
            </tr>
            <tr>
                <td>Creative curry</td>
                <td>$10</td>
            </tr>
            <tr>
                <td>Sloppy salmon</td>
                <td>$20</td>
            </tr>
        </table>
    </body>
</html>//显示的框的宽度与最长的一样
## CLASS RULES ##
<html>
    <head> 
        <style>
            table, td, th {border: 1px solid green; width:50%; text-align:center}
            .profit {text-align:left; background-color:lightblue}
            .zero {text-align:center; background-color:yellow}
            .loss {text-align:right; background-color:red}
        </style> 
    </head>
    <body>
        <table>
            <tr>
                <th>Product</th>
                <th>Income</th>
                <th>Cost</th>
                <th>Difference</th>
            </tr>
            <tr>
                <td>Laptops</td>
                <td>$300</td>
                <td>$100</td>
                <td class="profit">$200</td>
            </tr>
            <tr>
                <td>Stationary</td>
                <td>$150</td>
                <td>$150</td>
                <td class="zero">$0</td>
            </tr>
            <tr>
                <td>Chairs</td>
                <td>$50</td>
                <td>$300</td>
                <td class="loss">$250</td>
            </tr>
        </table>
    </body>
</html>//<tr>行，<th>头，<td> 标签定义 HTML 表格中的标准单元格。
## CLASS RULES ##
<html>
    <head> 
        <style>
            table, td, th {border: 1px solid green; width:75%;text-align:center}
            .profit {text-align:left; background-color:lightblue}
            .zero {text-align:center; background-color:yellow}
            .loss {text-align:right; background-color:red}
        </style> 
    </head>
    <body>
        <table>
            <tr>
                <th>Product</th>
                <th>Income</th>
                <th>Cost</th>
                <th>Difference</th>
            </tr>
            <tr>
                <td>Laptops</td>
                <td>$300</td>
                <td>$100</td>
                <td class="profit">$200</td>
            </tr>
            <tr>
                <td>Stationary</td>
                <td>$150</td>
                <td>$150</td>
                <td class="zero">$0</td>
            </tr>
            <tr>
                <td>Chairs</td>
                <td>$50</td>
                <td>$300</td>
                <td class="loss">$250</td>
            </tr>
        </table>
    </body>
</html>
## POSITIONING EXAMPLE ##
<html>
    <head>  
        <style>
            table, td {border:1px solid black; width:80%; height:80%}<!--定义了table表的大小，td的含义如果去除就没有边界线，其他的属性其实是在定义td的边接线宽一像素，实心黑线-->
            td {width:33.33%; height:33.33%}<!--这时候我再加一个呢？如果我再加一个则不会变大，会在整个大小的基础上压榨其他框的大小-->
            .t {vertical-align:top} .m {vertical-align:middle} .b {vertical-align:bottom}
            .l {text-align:left} .c {text-align:center} .r {text-align:right}
        </style>  
    </head>
    <body>
        <table>
            <tr>
                <td class="t l">1</td>
                <td class="t c">2</td>
                <td class="t r">3</td>
            </tr>
            <tr>
                <td class="m l">4</td>
                <td class="m c">5</td>
                <td class="m r">6</td>
            </tr>
            <tr>
                <td class="b l">7</td>
                <td class="b c">8</td>
                <td class="b r">9</td>
            </tr>
        </table>
    </body>
</html><!--{vertical-align:top},显示在单元格的上部分{text-align:left},文字显示在哪里-->
th ： table head ,定义表格内的表头单元格
td ： table data cell, 表格数据单元
tr： table row, 表格行
<thead> 标签定义表格的表头。该标签用于组合 HTML 表格的表头内容。thead 元素应该与 tbody 和 tfoot 元素结合起来使用。