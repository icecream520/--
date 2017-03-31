# STYLE #
## ELEMENTS & ATTRIBUTES WE WILL LOOK AT ##
<link>`href attribute`
       rel attribute
       type attribute
<style>
Any HTML element id attribute
## STYLE PROPERTIES WE WILL LOOK AT ##
Foreground color color
Background color background
## WE NEED STYLE! ##
We need to learn style
Without style your page is visually boring!
Style is also a major control feature for JavaScript libraries//风格样式是JavaScript库的主要控制功能
The language for style on the web is CSS,
Cascading Style Sheets
## THE GENERAL CONCEPT ##
We separate the information in the web page
from the visual properties used to display it
Information + Style = Visual Output
## 1 CSS FILE, MULTIPLE WEB PAGES ##
One CSS file can be used by multiple pages//一个css文件可以被多个页面使用
## LINKING TO A CSS FILE ##
<!DOCTYPE html>
<html>
<head>
<title>Demonstration of Linking to a Style File</title>
<link href="html_example_css_file.css" rel="stylesheet" type="text/css">
</head>
<body>
. . . elements which use the style rules go here . . .//像上表的使用，固定了<h></h><p></p>的颜色
</body>
</html>
## SIMPLE HTML FILE ##
    <!DOCTYPE html>
    <html>
    <head>
    <title>Demonstration of Linking to a Style File</title>
    <link href="html_example_css_file.css" rel="stylesheet" type="text/css">
    </head>
    <body>
    <h1>My first heading</h1>
    <p>My first paragraph</p>
    <h1>My second heading</h1>
    <p>My second paragraph</p>
    </body>
    </html>
SIMPLE CSS FILE//CSS文件的
    h1 { color:purple }
    p { color:blue }
## DEFINING STYLE AT THE TOP OF THE PAGE ##//在顶部定义页面样式
    <!DOCTYPE html>
    <html>
    <head>
    <style>
    . . . style rules for this web page go here . . .
    </style>
    </head>
    <body>
    . . . elements which use the style rules go here . . .
    </body>
    </html>

    <html>
    <head>
    <style>
    h1 {color:purple}
    p {color:blue}
    </style>
    </head>
    <body>
    <h1>My first heading</h1>
    <p>My first paragraph</p>
    <h1>My second heading</h1>
    <p>My second paragraph</p>
    </body>
    </html>
## USE A UNIQUE ID ##
Every element can have an id attribute
id has no effect for visual display//单单id对视图展示没有影响

    <html>
    <body>
    <ul id="rainbowColors">
    <li id="red">Red</li>
    <li id="orange">Orange</li>
    <li id="yellow">Yellow</li>
    <li id="green">Green</li>
    <li id="blue">Blue</li>
    <li id="indigo">Indigo</li>
    <li id="violet">Violet</li>
    </ul>
    </body>
    </html>
## USING ID FOR STYLE ##
You can use #id for select the target of the style rule
#theElementID {color: red}
STYLE USING ID <HEAD> PART
    <html>
    <head>
    <style>
    #rainbowColors {background: grey}
    #red {background: red}
    #orange {background: orange}
    #yellow {background: yellow}
    #green {background: green}
    #blue {background: blue}
    #indigo {background: indigo}
    #violet {background: violet}
    </style>
    </head>

    STYLE USING ID <BODY> PART
    <body>
    <ul id="rainbowColors">
    <li id="red">Red</li>
    <li id="orange">Orange</li>
    <li id="yellow">Yellow</li>
    <li id="green">Green</li>
    <li id="blue">Blue</li>
    <li id="indigo">Indigo</li>
    <li id="violet">Violet</li>
    </ul>
    </body>
    </html>
## USING CLASS ##
Make your own rule, apply to anything
One rule can be used for multiple elements
    <html>
      <head>
         <style>
    .zappy {color:purple; background:yellow}
    .wow {color:blue; background:lightgrey}
         </style>
      </head>
      <body>
    <h1 class="zappy">My first heading</h1>
    <p class="wow">My first paragraph</p>
    <h1 class="wow">My second heading</h1>
    <p class="zappy">My second paragraph</p>
      </body>
    </html>
## USING MULTIPLE CLASSES ##
One element can use multiple classes
    <html>
     <head>//注释掉head无所谓为了格式
      <style>
       .zappy {color:blue}
       .spicy {color:red}
       .wow {background:lime}
       .lol {background:lightgrey}//多种类自己拼接
      </style>
     </head>
     <body>
        <p class="zappy wow">My first paragraph</p>
        <p class="zappy lol">My second paragraph</p>
        <p class="spicy wow">My third paragraph</p>
        <p class="spicy lol">My fourth paragraph</p>
     </body>
    </html>
