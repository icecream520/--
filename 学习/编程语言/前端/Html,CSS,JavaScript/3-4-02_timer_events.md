#TIMER EVENTS#
## TIMERS ##
Timers are very useful for dynamic web page behaviour
Set a timer like this:
    var the_timer;
    the_timer=setTimeout(do_something, 1000);
do_something() will be executed 1 second later
The value 1000 is in milliseconds, so 1000=1 second
<html>
    <head>
        <script>
            var wait_duration;
            
            function set_things_up() {
                wait_duration = prompt("How long do you " +
                                       "want to sleep?");
                //得到时间
                setTimeout(show_wake_up_message, wait_duration );
                //setTimeout(do,time);
            }
            function show_wake_up_message() {
                alert("WAKE UP! WAKE UP! WAKE UP!!");
            }
        </script>
    </head>
    <body onload="set_things_up()">
        <h1>Alarm clock example</h1>
    </body>
</html>
### TIMER EXAMPLE - MOVING AN IMAGE ###
<html>
    <head>
        <script>
            var the_timer, x_position = 0, the_image;
            
            function set_timer() {
                the_image = document.getElementById("stones_img");
                //得到图片id取到图片
                x_position = x_position + 1;
                the_image.style.left = x_position;
                //改变图片的左边位置
                the_timer = setTimeout(set_timer, 50); 
                //近似于一秒X+1
            }
        </script>
    </head>
    <body onload="set_timer()">
        //加载完毕后就调用set_timer()
        <img src="stones.png" id="stones_img"
             style="position:absolute; left:0">
            //绝对位置，左边0点开始
        <button onclick="clearTimeout(the_timer)">
            //清除定时器
            Stop!
        </button>
    </body>
</html>
## STOPPING A TIMER ##
If a timer is started like this:
    var the_timer;
    the_timer=setTimeout(do_something, 1000);
Then stop it like this:
    clearTimeout(the_timer);
## SETINTERVAL ##
setInterval() repeatedly does something
Start it like this:
var the_timer;
the_timer=setInterval(do_something, 2000);
do_something() will be executed every 2 seconds
To stop it:
clearInterval(the_timer);

<html>
    <head>
        <script>
          var the_timer, x_position = 0, the_image;
          
          function do_timer(){
            the_image = document.getElementById("stones_img");
            x_position = x_position + 1;
            the_image.style.left = x_position;
          }
        </script>
    </head>
    <body onload="the_timer=setInterval(do_timer, 50)">
     <!--差别就是一个是调用的时候延迟调用，好像是差不多的-->
        <img src="stones.png" id="stones_img"
             style="position:absolute; left:0">
        <button onclick="clearInterval(the_timer)">
            Stop!
        </button>
    </body>
</html>
