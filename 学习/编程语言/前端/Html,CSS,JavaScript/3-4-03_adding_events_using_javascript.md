# ADDING EVENTS USING JAVASCRIPT #
## ADDING A HANDLER USING HTML ##
Adding an event to an element in HTML:
    <html><head><script>
     function do_something() {alert("Page has loaded");}
     </script></head>
     <body onload="do_something()"></body>
    </html>
do_something() is the event handler for this event
## ADDING A HANDLER USING JAVASCRIPT ##
We can also add an event to an element:
    <html><body id="theBody">
     <script>
     function do_something() { alert("Page has loaded") }
     window.onload = do_something;
     </script>
    </body></html>
Another way:
    <html><body>
    <script>
    function do_something() { alert("Page has loaded") }
    window.addEventListener("load", do_something);
    //window添加一个事件监听者("load的时候",do)
    </script>
    </body></html>
## IF YOU HAVE MORE THAN ONE EVENT HANDLER ##
Event handlers are stored in an array
When an event happens, all the handlers are executed
They are executed in the order they are added
## REMOVING AN EVENT HANDLER ##
REMOVING AN EVENT HANDLER
    var theBody = document.getElementById("theBody");
    theBody.removeEventListener("load", do_something);
<!doctype html>
//html5标准网页声明，原先的是一串很长的字符串，现在是这个简洁形式，支持html5标准的主流浏览器都认识这个声明。表示网页采用html5
<html>
    <body>
        <button id="btn0" onclick=" alert('Hello!') ">
            Click Me!</button><br>
        <button id="btn1">Remove Listener</button>
        //注意有先后顺序的要是加载前面会导致按钮ID还没哟出现就直接得到了，最好就是用ext或者是jQuery来先完成加载
        <script>
            function do_something() { alert('Clicked'); }

            var btn0 = document.getElementById("btn0");
            btn0.addEventListener("click", do_something);

            var btn1 = document.getElementById("btn1");
            btn1.addEventListener("click", function() {
              btn0.removeEventListener("click", do_something);
            });
        </script>
    </body>
</html>