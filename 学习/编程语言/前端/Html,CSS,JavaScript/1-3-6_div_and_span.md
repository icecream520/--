# DIV AND SPAN #
## ELEMENTS WE WILL LOOK AT ##
For a large area <div>
For a few words <span>
<div>	定义文档中的分区或节（division/section）。
<span>	定义 span，用来组合文档中的行内元素。
ELEMENTS WE WILL LOOK AT
For a large area <div>
For a few words <span>
## STYLE PROPERTIES WE WILL LOOK AT ##
font‐size font‐family
background position
top left
width
## DIV ##
div has no default style
div has no default meaning
HTML developers can use it for any purpose
<p>This is a paragraph before the div</p>

<div>
    This is a div with no style
</div>

<p>This is a paragraph in the middle</p>

<div style="background:lightblue">
    This is a div with a blue background
</div>
<!--<div>万能的老-->
<p>This is a paragraph before the div</p>

<div style="background:yellow; font-size:16pt; font-family:courier">
    This is a div with a yellow background
</div>

<p>This is a paragraph in the middle</p>

<div style="background:lightblue; font-size:18pt; font-family:Arial; width:50%">
    This is a div with a blue background
</div>
## POSITIONING AN ELEMENT ##
Like many elements, a div can be put anywhere
Use position:absolute with top:xxx and left:yyy
top and left refer(指) to the top left corner of the div
top:0 and left:0 means the div is in the top left corner
ABSOLUTE POSITION//绝对位置

<div style="background:yellow; font-size:16pt; font-family:courier; 
            position:absolute; top:60px; left:60px"><!--还是和其他语言一样没有变化位置越大Top越往下-->
    This is a div with a yellow background
</div>

<div style="background:lightblue; font-size:18pt; 
            position:absolute; top:92px; left:80px">
    This is a div with a blue background
</div>
## RELATIVE POSITION ##<!--相对位置-->
position:relative sets the position
relative to the normal position
    <p>This is a paragraph</p>
    
    <div style="background:yellow; font-size:14pt; font-family:courier; 
    position:relative; top:-20px; left:-20px">
    This is a div with a yellow background
    </div>
## SPAN ##
Like div, span has no default style
span is used for a few words
    <p>This is not span text <span>but this is</span> and this isn't</p>
    
    <p>This is not span text <span style="background:yellow">but this is</span> and this isn't</p>
2个都是用来划分区间但是没有实际语义的标签,差别就在于div是块级元素,不会其他元素在同一行;span是内联元素~可以与其他元素位于同一行~