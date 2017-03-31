# MAKING DECISIONS #
<!doctype html>
<html>
    <head>
        <script>
            var user_name;

            user_name=prompt("What is your name?");
            if (user_name == "dave")
                alert("Great name!");
        </script>
    </head>
</html>
## USING BRACES ##大括号
<!doctype html>
<html>
    <head>
        <script>
            var user_name;

            user_name=prompt("What is your name?");
            if (user_name == "dave")
                alert("Great name!");
            else
                alert("Your name isn't great...");
        </script>
    </head>
</html>

<!doctype html>
<html>
    <head>
        <script>
            var user_name;

            user_name=prompt("What is your name?");
            if (user_name == "dave")
                alert("Great name!");
            else if (user_name == "jogesh")
                alert("Pretty good name!");
        </script>
    </head>
</html>
<!doctype html>
<html>
    <head>
        <script>
            var user_name;

            user_name=prompt("What is your name?");
            if (user_name == "dave")
                alert("Great name!");
            else if (user_name == "jogesh")
                alert("Pretty good name!");
            else if (user_name == "oz")
                alert("Excellent name!");
            else
                alert("Your name isn't great, never mind...");
        </script>
    </head>
</html>
## switch case ##
break is used to stop any more case comparisons
Sometimes break is appropriate, sometimes it isn't
!doctype html>
<html>
    <head>
        <script>
        var user_name = prompt("What is your name?");

        switch(user_name) {
            case "dave":
                alert("Great name!"); 
                break;//记得break
            case "jogesh":
                alert("Pretty good name!"); 
                break;
            default:
                alert("Your name isn't great, never mind...");
        }
        </script>
    </head>
</html>

<!doctype html>
<html>
    <head>
        <script>
        var user_name = prompt("What country would you like to visit?");
        switch(user_name) {
            case "Canada":
            case "France":
                alert("Take me also!"); 
                break;
            case "Japan":
            case "Philippines":
                alert("Great! Have fun!"); 
                break;
            case "North Korea":
                alert("Oh! Good luck!"); 
                break;
            default:
                alert("I am sure you will have a great time");
        }
        </script>
    </head>
</html>
