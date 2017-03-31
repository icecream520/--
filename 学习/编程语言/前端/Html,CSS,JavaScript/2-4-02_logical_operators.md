# LOGICAL OPERATORS #
## BOOLEAN ##
A Boolean value is either true or false
A variable which has a Boolean value is called a
Boolean variable
<!doctype html>
<html>
    <body>
        <script>
            var you_are_rich = false;
            var you_have_partner = true;
            var you_have_flat = true;
            var life_is_fantastic = you_are_rich 
                                    && you_have_partner 
                                    && you_have_flat;
            
            alert("life is fantastic is " +
                   life_is_fantastic);
            you_are_rich = true;
            life_is_fantastic = you_are_rich 
                                && you_have_partner 
                                && you_have_flat;
            alert("life is fantastic is now " + 
                   life_is_fantastic);
        </script>
    </body>
</html>
## SHORT-CIRCUIT IN AND ##
JavaScript is clever
When it evaluates an And it checks the first input
If the value is false it knows the result must be false
So it doesn't bother checking the next input
<!doctype html>
<html>
    <head>
        <title>Not Operator Example</title>
    </head>
    <body>
        <script>
            var you_are_male = true;
            var you_are_female = !you_are_male;
            
            alert("you_are_male is " + you_are_male);
            alert("you_are_female is " + you_are_female);
        </script>		
    </body>
</html>