# 1-4-1_html_form_basics #
ELEMENTS & ATTRIBUTES WE WILL LOOK AT
<form> method attribute
action attribute
<textarea>
FROM BROWSER TO SERVER
Forms are the simplest method
The Browser
The Server
1. The user fills in a form and submits it
2. The browser sends the form data to the server
3. The server receives the data,processes it, sends a response
4. The browser displays the response
##  BASIC FORM STRUCTURE ##
<form action="destination" method="get or post">
. . . form elements go here . . .
<input type="submit">
</form>
### DESTINATION ###
action="destination" tells the browser
what program to send the form data to e.g.:
     <form action="http://www.server.com/subdirectory/program.php">
If the program is on same server as the html file:
     <form action="subdirectory/program.php">
If the program in same directory as the html file:
     <form action="program.php">
## GET OR POST ##
   method="get"
   get is the default method
   Example: search for cats using bing.com
   The URL will be http://www.bing.com/search?q=cats . . .
### THE GET METHOD ###
   For a project you are developing, using get is a good idea
   Seeing the form data in the URL is useful
   However, you cannot keep any secrets
   get can only handle a small transmission(少量信息传播)
   e.g. a few hundred letters/characters
### THE POST METHOD ###
   method="post"
   The main difference to get is you cannot see any data
   Using post is better for keeping secrets
   post can handle a big transmission e.g. files
SIMPLE EXAMPLE - TEXTAREA
<form>

    <p>Please enter any feedback you have.</p>

    <textarea rows="3" cols="60" name="feedback" >
        Please enter your text here
    </textarea>

</form>
## ADDING A SUBMIT BUTTON ##
<form action="http://ihome.ust.hk/~rossiter/cgi-bin/show_everything.php"
      method="get">
    <p>Please enter any feedback you have.</p>

    <textarea rows="3" cols="60" name="feedback" >
        Please enter your text here
    </textarea>
    <br>
    <input type="submit" value="Send">
</form>
<!--<textarea rows="3" cols="60" name="feedback">,row是行数，cols是每行长度，name是这行的名称-->
<!---->