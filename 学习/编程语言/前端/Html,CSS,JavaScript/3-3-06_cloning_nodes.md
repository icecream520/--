# CLONING NODES #
<!DOCTYPE html>
<html>
    <body>
        <script>
            function myFunction() {
                var the_node=document.getElementById("myList").lastChild;
                //就是说得到<li>
                var the_clone=the_node.cloneNode();
                document.getElementById("myList").appendChild(the_clone);
                //在<ul id="myList">下面添加子节点
            }
        </script>
        <ul id="myList">
        <li>Good morning</li>
        <li>Hello</li>
        </ul>
        <p>Click on the button to cloneNode()</p>
        <button onclick="myFunction()">Copy it!</button>
    </body>
</html>
## CLONING A BRANCH ##
Use node.cloneNode(true)
<!DOCTYPE html>
<html>
    <body>
        <script>
            function myFunction() {
                var the_node = document.getElementById("myList").lastChild;
                var the_clone = the_node.cloneNode(true);
                document.getElementById("myList").appendChild(the_clone);
            }
        </script>
        <ul id="myList"><li>Good morning</li><li>Hello</li></ul>
        <p>Click on the button to cloneNode(true)</p>
        <button onclick="myFunction()">
            Copy it!
        </button>
    </body>
</html>
        //clone的是节点还是Branch就看cloneNode()有没有true