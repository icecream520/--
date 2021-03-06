# AN EXAMPLE DOM PROJECT #
## HOW IT WORKS ##
A series of squares is generated by JavaScript
Each square is a div
Each square has a different
top, left, width and height
## HTML PART ##
position:absolute
定义和用法
position 属性规定元素的定位类型。
描述：absolute	
生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。
元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。
fixed	
生成绝对定位的元素，相对于浏览器窗口进行定位。
元素的位置通过 "left", "top", "right" 以及 "bottom" 属性进行规定。
relative	
生成相对定位的元素，相对于其正常位置进行定位。
因此，"left:20" 会向元素的 LEFT 位置添加 20 像素。
static	默认值。没有定位，元素出现在正常的流中（忽略 top, bottom, left, right 或者 z-index 声明）。
inherit	规定应该从父元素继承 position 属性的值。

<!doctype html>
<html>
    <head>
        <title>An Example Project</title>
        <meta http-equiv="refresh" content="1">
        <style>
            div {position:absolute} 
        </style>
    </head>
    <body id="theBody" onload="show_pattern()">
        <script src="01_dom_colorful_pattern_js.js">
        </script>
    </body>
</html>
The main code is triggered when the web page is loaded
    <body id="theBody" onload="show_pattern()">
The actual code is stored in another file:
    <script src="08_dom_colorful_pattern_js.js">
    </script>
This tells the browser to reload the page every second:
    <meta http­equiv="refresh" content="1">
## JAVASCRIPT OVERVIEW ##
Set up the variables
Inside the loop:
1. Generate the div node
2. Set the div node attributes
3. Add the div node to the body
4. Adjust variables ready for the next iteration
###SET UP THE VARIABLES###
    var top_position = 25, left_position = 25;
    var width = 300, height = 300;
    var color_list = ["red","orange","yellow",
    "green","blue","indigo","violet"];
### WHILE LOOP STRUCTURE ###
    while (width > 50) {
    // all the following code goes here
    }
#### GENERATE THE DIV NODE ####
    var this_div = document.createElement("div");
#### 2. SET THE DIV NODE ATTRIBUTES ####
    var random_color = Math.random() * 7;
    random_color = Math.floor(random_color);
    this_div.style.top = top_position + "px";
    this_div.style.left = left_position + "px";
    this_div.style.width = width + "px";
    this_div.style.height = height + "px";
    this_div.style.background =
    color_list[random_color];
#### 3. ADD THE DIV NODE TO THE BODY ####
    var the_body = document.getElementById("theBody");
    the_body.appendChild(this_div);
#### 4. ADJUST VARIABLES ####
    top_position += 10;
    left_position += 10;
    width ­= 20;
    height ­= 20;
function show_pattern(){
    var top_position = 25, left_position = 25; 
    var width = 500, height = 500;
    var color_list = ["red","orange","yellow","green","blue","indigo","violet"];
    var the_body = document.getElementById("theBody");
					  
    while(width > 50) {
        var this_div = document.createElement("div");                  
        var random_color = Math.random() * 7;
        random_color = Math.floor(random_color);
        this_div.style.top = top_position + "px";
        this_div.style.left = left_position + "px";
        this_div.style.width = width + "px";
        this_div.style.height = height + "px";
        this_div.style.background = color_list[random_color];
        the_body.appendChild(this_div);
        top_position += 10; left_position += 10;
        width -= 20; height -= 20;
    }
}