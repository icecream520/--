## CSS 链接 ##
不同的链接可以有不同的样式。
链接样式
链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。
特别的链接，可以有不同的样式，这取决于他们是什么状态。
这四个链接状态是：
a:link - 正常，未访问过的链接
a:visited - 用户已访问过的链接
a:hover - 当用户鼠标放在链接上时
a:active - 链接被点击的那一刻
实例
a:link {color:#FF0000;}      /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 已访问过的链接 */
当设置为若干链路状态的样式，也有一些顺序规则：
a:hover 必须跟在 a:link 和 a:visited后面
a:active 必须跟在 a:hover后面
常见的链接样式
根据上述链接的颜色变化的例子，看它是在什么状态。
让我们通过一些其他常见的方式转到链接样式：
文本修饰
text-decoration 属性主要用于删除链接中的下划线：
实例
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:underline;}
a:active {text-decoration:underline;}
## 背景颜色 ##
背景颜色属性指定链接背景色：
实例
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}

//原来也可以为link设置超链接class,然后是a.class设置属性，
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="utf-8"> 
    <title>菜鸟教程(runoob.com)</title> 
    <style>
    a.one:link {color:#ff0000;}
    a.one:visited {color:#0000ff;}
    a.one:hover {color:#ffcc00;}
    
    a.two:link {color:#ff0000;}
    a.two:visited {color:#0000ff;}
    a.two:hover {font-size:150%;}
    
    a.three:link {color:#ff0000;}
    a.three:visited {color:#0000ff;}
    a.three:hover {background:#66ff66;}
    
    a.four:link {color:#ff0000;}
    a.four:visited {color:#0000ff;}
    a.four:hover {font-family:monospace;}
    
    a.five:link {color:#ff0000;text-decoration:none;}
    a.five:visited {color:#0000ff;text-decoration:none;}
    a.five:hover {text-decoration:underline;}
    </style>
    </head>
    
    <body>
    <p>将鼠标移至链接上改变样式.</p>
    
    <p><b><a class="one" href="/css/" target="_blank">This link changes color</a></b></p>
    <p><b><a class="two" href="/css/" target="_blank">This link changes font-size</a></b></p>
    <p><b><a class="three" href="/css/" target="_blank">This link changes background-color</a></b></p>
    <p><b><a class="four" href="/css/" target="_blank">This link changes font-family</a></b></p>
    <p><b><a class="five" href="/css/" target="_blank">This link changes text-decoration</a></b></p>
    </body>
    
    </html>