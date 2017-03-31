# THE DOM - BASIC CONCEPTS #
## THE DOM ##
DOM means Document Object Model//文本对象模型
When you load something into a browser,
it is converted into a DOM structure
CODE WE HAVE SEEN
<!DOCTYPE html>
<html>
    <head>
        <title>A Simple Web Page</title>
        <meta name="author" content="David Rossiter">
    </head>
    <body>
        <h1>My Web Page</h1>
        <p>This web page is so awesome!</p>
    </body>
</html>

<!DOCTYPE html>
<html>
    <body>
        <table> 
            <tbody>
                <tr> //行row
                    <td>Oz</td> //Tabele date cell
                    <td>28</td> 
                </tr>
                <tr> 
                    <td>Budi</td> 
                    <td>19</td> 
                </tr>
            </tbody>
        </table>
    </body>
</html>

<!DOCTYPE html>
<html>
    <body id="theBody"><p id="firstP">
        Hi there!
        </p>
        How are you?
        <br>
        <p id="secondP">
            It's a nice day!
        </p>
    </body>
</html>
## WHITESPACE NODES ##
Whitespace is anything you can't see i.e. spacing
There may be a text node which contains only whitespace
These is called a 'whitespace node'
These are sometimes troublesome
## A COMPARISON ##
    <body><p>Hello.</p>
does not have a whitespace node between  <body> and <p>
<body>
<p>Hello.</p>
have a whitespace node between <body> and <p>
<!DOCTYPE html>
<html>
    <body id="theBody">
        <p id="firstP">
            Hi there!
        </p>
        How are you?
    </body>
</html>

