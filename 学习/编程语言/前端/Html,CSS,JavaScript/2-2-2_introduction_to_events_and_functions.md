# INTRODUCTION TO EVENTS AND FUNCTIONS #
## AFTER THIS PRESENTATION ##
You'll appreciate the concept(概念) of events
You'll understand how to use functions
## EVENTS ##
An event is when something happens
For example:
Click on something
Move the mouse
Press a key on the keyboard
You can arrange(排列) for some code that you write
to be executed(执行) when the event occurs（发生）
## ONLOAD EVENT ##
onload is triggered when the object has loaded
<body onload="alert('Hello!')">
. . . the main web page content goes here . . .
</body>

<!doctype html>
<html>
    <body onload="alert('Hello!')">//加载完成即跳出alert
        <p>
            A message is shown as soon 
            as the page is loaded.
        </p>
    </body>
</html>

<!doctype html>
<html>
    <body onload="alert('Hello!');
                  alert('We start soon...');
                  prompt('Excited?!') ">
        <p>
            3 popup windows are shown as  
            soon as the page is loaded.
        </p>
    </body>
</html>
## FUNCTIONS ##
A function is a group of code:
function do_something() {
. . . code goes here . . .
}
Run the function like this:
do_something();

<!doctype html>
<html>
    <head>
        <title>Example of a function</title>
        <script>
            function greet_the_user(){
                alert('Hello!');
                alert('We start soon...');
                prompt('Excited?!')
            }
        </script>
    </head>
    <body onload="greet_the_user()">
    </body>
</html>
## FUNCTION PARAMETERS ##
You can pass something to a function
function purchase( cats ) {
 . . code here uses cats . . .
}
Run the function like this:
purchase( 10 );
### FUNCTION RESPONSE ###
function do_something() {
. . . code here stores something in answer . . .
return answer; 
}
Use the function like this:
result = do_something();

<!doctype html>
<html>
    <body onload="check_user_age()">//刚加载的时候时候调用这个方法
        <h1>This is my naughty home page.</h1>
        <script>
            function check_user_age(){
                if (age_of_user() < 18)//调用这个方法得到年龄
                    alert("Please go to another page.");//比较
            }
            function age_of_user(){
                var age_text, age;//新建两个变量
                age_text=prompt("What is your age?");//得到string※年龄
                age=parseInt(age_text);//转成int
                return age;//返回年龄
            }
        </script>
    </body>
</html>

## A RECURSIVE FUNCTION ##//递归函数
A function can call itself
function do_something( control_value ) {
. . . code here calls do_something( . . . )
}
Start the function like this:
result = do_something( 10 );

<!doctype html>
<html>
    <body>
        <script>
            alert("It's my " + build_great(5) +
                  "grandmother!");//跳出It's my 调用传参

            function build_great( depth ) {
                if (depth > 0)
                    return "great " + build_great( depth - 1 );
                else
                    return "";
            }
        </script>
    </body>
</html>
