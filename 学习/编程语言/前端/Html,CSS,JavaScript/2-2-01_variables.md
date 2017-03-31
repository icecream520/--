# VARIABLES #
## NUMBER ##
JavaScript has only one type of number
Can be written with or without a decimal place
var number1 = 34.289;
var number2 = 100;
Can use scientific notation
var big_number = 123e5; //12300000
var small_number = 123e­5; //0.00123
## STRING ##
Astring simply means text
You can use single or double quotes
var name = "David";
var title = 'Professor';
You can use quotes inside a string, as long as they
don't match the quotes surrounding the string
var message = "It's alright";
## BOOLEAN ##
A Boolean value can only be true or false
var condition1 = true;
var condition2 = false;
Do not confuse Boolean values with String values
var myBool = true; //Boolean type
var myString = "true"; //String type
## USING TYPEOF ##
<!doctype html>
<html>
    <head>
        <title>Variable Type Example</title>
    </head>
    <body>
        <script>
            alert( '"John" is type: ' + typeof "John" + "\n\n"
                   + "3.14 is type: " + typeof 3.14 + "\n\n"
                   + "false is type: " + typeof false ) ;
        </script>
　　　　　//typeof""可以直接得到数据类型
    </body>
</html>
