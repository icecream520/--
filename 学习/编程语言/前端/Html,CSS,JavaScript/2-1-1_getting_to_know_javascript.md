# ABOUT JAVASCRIPT #
## JAVASCRIPT POPULARITY ##
Server application
Node.js modules
Node.js
MongoDB
## JAVASCRIPT FUNCTIONS WE WILL LOOK AT ##
alert()
prompt()
confirm()
## WHERE TO PUT JAVASCRIPT? ##
- JavaScript code can go almost anywhere
- However, there is a common pattern
<!DOCTYPE html>
<html>
 <head>
. . . load JavaScript libraries here . . .
 </head>
 <body>
. . . your JavaScript code typically goes at the end of body . . .
 </body>
</html>
### JAVASCRIPT IN THE SAME FILE ###
<script>
    function surprise() { 
        alert("Hello!");
    }
</script>
### JAVASCRIPT IN ANOTHER FILE ###
<script src="mycode.js"></script>
In mycode.js:
function surprise() {
alert("Hello!");
}
### SIMPLE INTERACTION ###
There are 3 JavaScript popups:
1. alert()
2. confirm()
3. prompt()
## MAKING A DECISION - CONFIRM() ##<!--confirm()决策，可以取消，可以确定-->
confirm() displays a popup box with a message,
along with an OK and a Cancel button
<!doctype html>
<html>
    <head>
        <title>Example of confirm()</title>
        <script>
            if (confirm("Want to go to Disneyland?")) 
                document.location.href="http://www.baidu.com"
        </script>
		<!--="http://park.hongkongdisneyland.com";-->
    </head>
</html>
## VARIABLES ##
A variable is like a box
You can make a variable and put something in it e.g
    var totalCost = 7000;
Later, you can take it out of the box and use it
You can change what is stored in the box any time
## SIMPLE TEXT INPUT - PROMPT() ##
For getting input from the user, you can
use prompt(), e.g://用于获取用户输入
    var user_name; // Create a variable
    user_name=prompt("What is your name?");
You don't have to create a variable before you use it
However, it is good habit to get into

<!doctype html>
<html>
    <head>
        <title>Example of prompt()</title>
        <script>
            var user_name;
            
            user_name = prompt("What is your name?");
             <!--prompt里面是用户输入的文本文本-->
            document.write("Welcome to my page "
                           + user_name + "!" );
        </script>
    </head>
</html>
