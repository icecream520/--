#NODE RELATIONSHIPS#
previousSibling//该属性表示当前节点的下一个节点（其后的节点与当前节点同属一个级别）；如果其后没有与其同级的节点，则返回null。 , nextSibling//该属性与nextSibling属性的作用正好相反。例如：someTagObject.nextSibling.previousSibling其实返回的是该标签元素本身，但前提必须是：该标签元素的后面必须有一个同级的元素，否则就返回null了。
access 访问
## HOW TO FIND THE PATH? ##
In the next example we show the path to a node

1. The function starts with a node
2. The type of the node is added to a string
3. The code moves to the parent of the node
4. If the node has a parent, repeat (2) and (3)
 function handleClick(event) {
            event.stopPropagation();

            var node = event.target
            var thisPath = node.nodeName;

            while (node.parentNode) {
                node = node.parentNode;
                thisPath = node.nodeName + " > " + thisPath;
            }
            alert(thisPath);
        } 
## HOW TO TRIGGER THE CODE? ##
To trigger the code, the user clicks on a node
To enable this, event handlers are added to the nodes


        // Register the click event handler for all nodes
        function attachHandler(node) {
            if(node == null) return;
            node.onclick = handleClick;

            for(var i = 0; i < node.childNodes.length; ++i) {
                visit(node.childNodes[i]);
            }
        }
