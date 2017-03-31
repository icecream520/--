# MOUSE EVENTS #

## MOUSE EVENTS ##
The most commonly used mouse events:
onclick - when the user clicks on an object
onmousedown - when the user presses down the mouse button
onmouseup - when the user lets go of the mouse button
onclick = onmousedown followed by onmouseup//onclick等于两个的集合
<!DOCTYPE html>
<html>
    <body>
        <script>
            function good_choice() { 
                alert("Good choice!"); 
            }
            function bad_choice() { 
                alert("I don't agree!"); 
            }
        </script>
        <h1>Click on the best social network...</h1>
        <img src="facebook_icon.png"
             onclick="bad_choice()">
        <img src="google_plus_icon.png"
             onclick="bad_choice()">
        <img src="twitter_icon.png"
             onclick="good_choice()">
    </body>
</html>
## MORE MOUSE EVENTS ##
onmouseover - mouse is moved over an object//鼠标扫过
onmouseout - mouse is moved away from an object//鼠标移出