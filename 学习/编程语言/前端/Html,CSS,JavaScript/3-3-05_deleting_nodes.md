# DELETING NODES #
## DELETING A NODE ##
Tell the parent of the node to delete it e.g
this_node=getElementById("myPara");
this_node.parentNode.removeChild(this_node);

    Three example code to delete the first paragraph in this DOM:
    var the_node=document.getElementById("firstP");
    the_node.parentNode.removeChild(the_node);
    or//得到元素ID
    var the_node=document.getElementsByTagName("p")[0];
    the_node.parentNode.removeChild(the_node);
    or//得到元素标签为<p>的第一个<p>
    var the_parent=document.getElementById("theBody");
    the_parent.removeChild(the_parent.firstChild);
     //得到id为body的第一个子元素

## THREE EXAMPLE CODE ##
    var the_node=document.getElementById("firstP");
    the_node.parentNode.removeChild(the_node);
    var the_node=document.getElementsByTagName("p")[0];
    the_node.parentNode.removeChild(the_node);
    var the_parent=document.getElementById("theBody");
    the_parent.removeChild(the_parent.firstChild);

<!DOCTYPE html>
<html>
    <head>
        <script>
            function delete1()
            {
                var the_node=document.getElementById("firstP");
                the_node.parentNode.removeChild(the_node);
                //一开始都是删除hello,这个只能删除一个很好理解，删除id固定的元素
            }
            function delete2()
            {
                var the_node=document.getElementsByTagName("p")[0];
                the_node.parentNode.removeChild(the_node);
                //所有<p>的第一个,然后second,然后reload，how are you不会删除，因为不是<p></p>
            }
            function delete3()
            {	
                var the_parent=document.getElementById("theBody");
                the_parent.removeChild(the_parent.firstChild);
                //得到thebody，然后删除下面的第一个，然后挨个删除
            }
        </script>
    </head>

    <body id="theBody">//父<p id="firstP">//子1
        Hello.//<子1的子1>
        </p>//<子2>
        How are you?//<子2的子1>
        <br>
        <p id="secondP">
        It's a nice day!
        </p>

        <button type="button" onclick="delete1()">Example 1</button>
        <button type="button" onclick="delete2()">Example 2</button>
        <button type="button" onmousedown="delete3()">Example 3</button>
        <p>
        Reload the page to reset the DOM.
        </p>
    </body>
</html>
## DELETING ALL CHILDREN ##
    var theNode = document.getElementById("theBody");
    while (theNode.firstChild) // While there is a child
    theNode.removeChild(theNode.firstChild);

<!DOCTYPE html>
<html> 
    <head> 
        <script>
            function delete_all_children() {
                var theNode = document.getElementById("theBody"); 
                while (theNode.firstChild) 
                    theNode.removeChild(theNode.firstChild);
            }
        </script> 
    </head> 
    
    <body id="theBody">
        <p id="firstP">Hello.</p>
        How are you?
        <br>
        <p id="secondP">It's a nice day!</p>
        <button type="button" onclick="delete_all_children()">
            Delete children
        </button>
    </body> 
</html>
