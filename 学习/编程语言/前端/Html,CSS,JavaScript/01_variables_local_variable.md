#MORE ON VARIABLES#
## LOCAL VARIABLES ##
Variables declared (声明)within a function
can only be accessed（使用） within the function
They are local to the function,
and so are called local variables
<!doctype html>
<html>
    <body>
        <script>
            function show_money() {
                var money = 2;
                
                alert("In the function, the value is: "+ money);
            }
            money = 99;
            
            alert("In the main part, the value is: "+ money);
            show_money();
            alert("In the main part, the value is: "+ money);
        </script>
    </body>
</html>
## GLOBAL VARIABLES ##
The opposite of a local variable is a global variable
Global variables are created in the main part
They can work inside or outside functions
<!doctype html>
<html>
    <body>
        <script>
            function show_money() {
                alert("In the function, the value is: "+ money);
            }
            var money = 99;
            
            alert("In the main part, the value is: "+ money);
            show_money();
            alert("In the main part, the value is: "+ money);
        </script>
    </body>
</html>
If you assign a value to a variable that has not been
declared, it will automatically become a global variable
//他的意思是如果有个变量在函数内部声明，如果你没有再次声明就调用了它，那么他自动变为全局变量
<!doctype html>
<html>
    <body>
        <script>
            function show_money() {
              money = 2;
              
              alert("In the function, the value is: "+ money);
            }
            show_money();
            alert("In the main part, the value is: "+ money);
        </script>
    </body>
</html>
