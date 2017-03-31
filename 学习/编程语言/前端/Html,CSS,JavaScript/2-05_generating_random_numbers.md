# GENERATING RANDOM NUMBERS #
Math.random()
Math.floor()//lua中的一个函数,math.floor(x)返回小于参数x的最大整数,即对浮点数向下取整.
## GENERATING A RANDOM NUMBER ##
You can generate a random number like this:
var random_number = Math.random();
The resulting range is [0, 1)
1 will not be generated
<!doctype html>
<html>
    <body>
        <script>
            var random_number;
            
            random_number = Math.random();
            alert( random_number );
			random = Math.random();
			prompt(random);
        </script>
    </body>
</html>

## SETTING UP THE RANGE ##//设置范围
So far the random number is in the range 0 up to 1
Multiply in order to get the range you want, i.e.
random_number = Math.random() * max_value;
We now have a number in the range [0, max_value)
<!doctype html>
<html>
    <body>
        <script>
            var random_number;
            
            random_number = Math.random() * 8;
            alert("Random number in the range 0 to " + 
                  "7.9999999:\n" + random_number );
        </script>
    </body>
</html>
## THROW AWAY THE DECIMAL PLACE ##
There is still a decimal place
Math.floor() dumps the decimal place//自动舍弃小数部分
For example, 2.82248 becomes 2

<!doctype html>
<html>
    <body>
        <script>
            var random_number;
             
            random_number = Math.random() * 50;
            random_number = Math.floor( random_number );
            alert("Random number in the range 0 to 49: " + 
                   random_number);
        </script>
    </body>
</html>