# MORE ON FORMS #
## ELEMENTS WE WILL LOOK AT ##
<select> <option>
<input type="text"> <input type="password">
<input type="checkbox"> <input type="radio">
## ATTRIBUTES WE WILL LOOK AT ##
placeholder attribute
value attribute
autofocus attribute
required attribute
### A REMINDER ###
<form action="http://ihome.ust.hk/~rossiter/cgi-bin/show_everything.php"
      method="get">
    <p>Please enter any feedback you have.</p>

    <textarea rows="3" cols="60" name="feedback" >
        Please enter your text here
    </textarea>
    <br>
    <input type="submit" value="Send">
</form>
### FORM INPUT ELEMENTS ###
Submit button <input type="submit">
Plain text <input type="text">
Checkbox <input type="checkbox">
Radio button <input type="radio">
Password field <input type="password">
<form>
    Please enter your name. <br>
    <input type="text" name="feedback"> <br> <br><!--单纯的文本输入-->

    Please select each of the following that you have. <br>
    <input type="checkbox" name="items" value="car">Car <br>
    <input type="checkbox" name="items" value="teddy bear">Teddy bear <br>
    <input type="checkbox" name="items" value="toothbrush">Toothbrush <br> <br><!--正方形，选中打钩-->
	
    Please indicate your intelligence level. <br>
    <input type="radio" name="iq" value="high">High <br>
    <input type="radio" name="iq" value="medium" checked>Medium <br>
    <input type="radio" name="iq" value="low">Low <br> <br><!--默认圆形，checked则中心已经打点-->
</form>
## PASSWORD ##
<form>
    <p>What is the secret password?</p>
    <input type="password" name="userpassword"> <br>
</form>

<form action="http://ihome.ust.hk/~rossiter/cgi-bin/show_everything.php">
    <p>What is the secret password?</p>
    <input type="password" name="userpassword"> <br>	

    <input type="submit" value="Send">
</form>

## SELECTING FROM A LIST ##
<form>
	<p>What city would you like to go to?</p>
	
	<select name="cities">
		<option value="hk">Hong Kong</option>
		<option value="vc">Vancouver</option>
		<option value="sf">San Francisco</option>
	</select>
</form><!--选中列，点击此列可以选择，两个同事selected,选择最后的
-->
## USEFUL ATTRIBUTES ##
value="something" fixes what is shown at the start
placeholder(占位符)="something" shows useful text which disappears
when the user enters something
autofocus sets which field is given focus at the start
required means this field must be completed

<form>
    <p>Please fill in the following information:</p><!--显示内容-->

    <label for="firstname">First name:</label><!--label for属性规定 label 与哪个表单元素绑定。-->
    <input type="text" name="firstname" value="Dave" autofocus>
    <br>
    <label for="lastname">Last name:</label>
    <input type="text" name="lastname" placeholder="Your last name goes here"><!--输入text文本，占位符为：-->
    <br>
    <label for="age">Age:</label>
    <input type="text" name="age" required><!--显示必填，不填跳出警告请填写此字段-->
    <br>
    <input type="submit" value="Submit"><!--按钮为submit控制form-->
</form>