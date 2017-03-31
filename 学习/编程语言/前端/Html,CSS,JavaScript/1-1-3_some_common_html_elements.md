TinyMCE 一款编辑器

   ##  ELEMENTS WE WILL LOOK AT ##
    Headings <h1> <h2> <h3> <h4> <h5> <h6>
    Sections <section>
    Lists <ul> and <ol> together with <li>
    Comments <!‐‐ a comment ‐‐>
    <section> is used to indicate a section//段落用来标识一个段落
## A SIMPLE LIST USING BULLETS ##//一个简单的子弹？列表
Now let's consider HTML lists//现在让我们考虑HTML列表
    <ul> means unordered list, <li> means list item//<ul>表示无序列表<li>表示列表方法
    <ul>
    <li>The first item</li>
    <li>The second item...</li>
    <li>Yes... the third item!</li>
    </ul>
## A SIMPLE LIST USING NUMBERS ##//简单列对数字的使用
    <ol> means ordered list//表示有序列
    <ol>
    <li>The first item</li>
    <li>The second item...</li>
    <li>Yes... the third item!</li>
    </ol>
1. The first item
2. The second item...
3. Yes... the third item! //同样三句话，无序列前面加个点，有序列有序列号
## CHANGING THE START NUMBER ##
Add start="number" to fix the starting number//在开始前面加数字来固定起始位置
    <ol start="1999">
    <li>In this year I was born...</li>
    <li>In this year I learned to walk...</li>
    <li>In this year I learned to program...</li>
    <li>In this year I learned SPA techniques...</li>
    </ol>
    1999. In this year I was born...
    2000. In this year I learned to walk...
    2001. In this year I learned to
    program...
    2002. In this year I learned SPA
    techniques...

## REVERSING THE ORDER ##//倒叙排列
Add reversed to reverse the order //添加reversed来让数字倒叙开始
    <ol start="2002" reversed>
    <li>In this year I learned SPA techniques...</li>
    <li>In this year I learned to program...</li>
    <li>In this year I learned to walk...</li>
    <li>In this year I was born...</li>
    </ol>
2002. In this year I learned SPA
techniques...
2001. In this year I learned to
program...
2000. In this year I learned to walk...
1999. In this year I was born... 
##  USING A LETTER ##//使用字母
Add type="A" to use a letter //只能A不能从B开始
    <ol type="A">
    <li>is for 'Anchor'...</li>
    <li>is for 'Body'...</li>
    <li>is for 'Cdata'...</li>
    <li>is for 'Div'...</li>
    </ol>
## COMMENTS ##//评论，备注
A comment looks like this: <!‐‐ a comment ‐‐>
    <html>
    <!­­ This is a simple demonstration of using comments in a web page ­­>
    <head>
    <meta name="author" content="David Rossiter">
    <!­­ I can't believe how amazing that guy really is! ­­>
    </head>
    <body>
    <!­­ Here's my simple 'to do' list ­­>
    <p>Items I need to fix in my business:</p>
    <ol> <li>The people</li>
    <li>The process</li>
    <li>The product</li> </ol>
    <!­­ That's a lot of things to fix! I better get started soon. ­­>
    </body>
    </html>