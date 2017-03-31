# CSS 表格 #
使用CSS可以大大提高HTML表格的外观。
Company	Contact	Country
Alfreds Futterkiste	Maria Anders	Germany
Berglunds snabbköp	Christina Berglund	Sweden
Centro comercial Moctezuma	Francisco Chang	Mexico
Ernst Handel	Roland Mendel	Austria
Island Trading	Helen Bennett	UK
Königlich Essen	Philip Cramer	Germany
Laughing Bacchus Winecellars	Yoshi Tannamuri	Canada
Magazzini Alimentari Riuniti	Giovanni Rovelli	Italy
North/South	Simon Crowther	UK
Paris spécialités	Marie Bertrand	France
The Big Cheese	Liz Nixon	USA
Vaffeljernet	Palle Ibsen	Denmark
## 表格边框 ##
指定CSS表格边框，使用border属性。
下面的例子指定了一个表格的Th和TD元素的黑色边框：
实例
table, th, td
{
border: 1px solid black;
}
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    <style>
    table, th, td {
    	border: 1px solid black;
    }
    </style>
    </head>
    
    <body>
    <table>//一张表
      <tr>//一row
    <th>Firstname</th>//thead
    <th>Lastname</th>
      </tr>
      <tr>
    <td>Peter</td>//tdata
    <td>Griffin</td>
      </tr>
      <tr>
    <td>Lois</td>
    <td>Griffin</td>
      </tr>
    </table>
    </body>
    </html>

请注意，在上面的例子中的表格有双边框。这是因为表和th/ td元素有独立的边界。
为了显示一个表的单个边框，使用 border-collapse属性。

## 折叠边框 ##
    border-collapse 属性设置表格的边框是否被折叠成一个单一的边框或隔开：
    实例
    table
    {
    border-collapse:collapse;//使本来td和th的边界折叠
    }
    table,th, td
    {
    border: 1px solid black;
    }
请注意，在上面的例子中的表格有双边框。这是因为表和th/ td元素有独立的边界。
为了显示一个表的单个边框，使用 border-collapse属性。
## 表格宽度和高度 ##
Width和height属性定义表格的宽度和高度。
下面的例子是设置100％的宽度，50像素的th元素的高度的表格：
实例
table 
{
width:100%;
}
th
{
height:50px;
}
## 表格文字对齐 ##
表格中的文本对齐和垂直对齐属性。
text-align属性设置水平对齐方式，像左，右，或中心：
实例
td
{
text-align:right;
}
垂直对齐属性设置垂直对齐，比如顶部，底部或中间：
实例
td
{
height:50px;
vertical-align:bottom;
}
## 表格填充 ##
如果在表的内容中控制空格之间的边框，应使用td和th元素的填充属性：
实例
td
{
padding:15px;
}
## 表格颜色 ##
下面的例子指定边框的颜色，和th元素的文本和背景颜色：
实例
table, td, th
{
border:1px solid green;
}
th
{
background-color:green;
color:white;
}


    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8">
    <title>菜鸟教程(runoob.com)</title>
    <style>
    #customers {
    	font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
    	width: 100%;
    	border-collapse: collapse;
    }
    #customers td, #customers th {
    	font-size: 1em;
    	border: 1px solid #98bf21;
    	padding: 3px 7px 2px 7px;
    }
    #customers th {
    	font-size: 1.1em;
    	text-align: left;
    	padding-top: 5px;
    	padding-bottom: 4px;
    	background-color: #A7C942;
    	color: #ffffff;
    }
    #customers tr.alt td {
    	color: #000000;
    	background-color: #EAF2D3;
    }
    </style>
    </head>
    ​
    <body>
    <table id="customers">
    <tr>
      <th>Company</th>
      <th>Contact</th>
      <th>Country</th>
    </tr>
    <tr>
      <td>Alfreds Futterkiste</td>
      <td>Maria Anders</td>
      <td>Germany</td>
    </tr>
    <tr class="alt">
      <td>Berglunds snabbköp</td>
      <td>Christina Berglund</td>
      <td>Sweden</td>
    </tr>
    <tr>
      <td>Centro comercial Moctezuma</td>
      <td>Francisco Chang</td>
      <td>Mexico</td>
    </tr>
    <tr class="alt">
      <td>Ernst Handel</td>
      <td>Roland Mendel</td>
      <td>Austria</td>
    </tr>
    运行结果： 菜鸟工具 
