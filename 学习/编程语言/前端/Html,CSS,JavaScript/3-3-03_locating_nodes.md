# LOCATING NODES #
USING THE EXACT PATH
Method 1: Use the exact DOM path
Sometimes hard to work out the exact path
Easy to make mistakes
In another browser the DOM may be slightly different
- code fails!
## - USING THE TYPE ##
Method 2: Use getElementsByTagName()
This requires you to know the exact tag name
e.g. is it h2 or h3?
There might be several nodes of that type,
so you have to know exactly which one it is
## USING THE NAME ##
Method 3: Use getElementById()
If you give a node a unique name e.g.
<element_name id="thing"> . . . </element_name>
then this method is the easiest way
 <body>
        <h2 style="color:black" id="cute_text">
            Click on a button to change the colour of this text
        </h2>
        <form>
            <input onclick="change_color1()" type="button" value="Change using method 1">
            <input onclick="change_color2()" type="button" value="Change using method 2">
            <input onclick="change_color3()" type="button" value="Change using method 3">
        </form>
 </body>

EXAMPLE - CODE
<!DOCTYPE html>
<html> 
    <head>
        <script>
            function change_color1() {
                document.childNodes[1].childNodes[2].childNodes[1].style.color="red";//文本所在位置,childNodes[1],指向了Body
            }

            function change_color2() {
                document.getElementsByTagName("h2")[0].style.color="yellow";
            }

            function change_color3() {
                document.getElementById("cute_text").style.color="blue";
            }
        </script>
    </head>

    <body>
        <h2 style="color:black" id="cute_text">
            Click on a button to change the colour of this text
        </h2>
        <form>
            <input onclick="change_color1()" type="button" value="Change using method 1">
            <input onclick="change_color2()" type="button" value="Change using method 2">
            <input onclick="change_color3()" type="button" value="Change using method 3">
        </form>
    </body>
</html>
## SETATTRIBUTE() ##
This is a common way to change something
For example:
    the_node=getElementById("thisNode");
    the_node.setAttribute("style", "color:red");
    <!DOCTYPE html>
      <html>
       <head>
        <script>
          function change_color1(){
          document.childNodes[0].childNodes[2].childNodes[1]
         .setAttribute("style", "color:red");
          }
          function change_color2(){
          document.getElementsByTagName("h2")[0]
         .setAttribute("style", "color:yellow");
       }
          function change_color3(){
          document.getElementById("cute_text")
         .setAttribute("style", "color:blue");
    }
     </script>
    </head>