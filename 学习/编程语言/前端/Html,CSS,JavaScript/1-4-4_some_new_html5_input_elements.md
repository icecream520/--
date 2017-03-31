# SOME NEW HTML5 INPUT ELEMENTS #
## ELEMENTS & ATTRIBUTES WE WILL LOOK AT ##
<input type="number">
<input type="date">
<input type="color">
<input type="range">
<input type="time">
## NEW HTML5 INPUT ELEMENTS ##
Number Input <input type="number">
Date Input <input type="date">
Time Input <input type="time">
Color Picker <input type="color">
Slider <input type="range">
例：
    <form action="http://ihome.ust.hk/~rossiter/cgi-bin/show_everything.php">!--<HTML <form> 标签的 action 属性下面的表单拥有两个输入字段以及一个提交按钮，当提交表单时，表单数据会提交到名为 "form_action.asp" 的页面：-->
      <label for="age">Your age:</label>
      <input type="number" min="0" max="99" step="1" value="18" id="age" name="age" required><br><!--type number 可以箭头选择，也可以直接填写，step代表箭头每次点击减少或增加的值，value为默认值，必填-->
      <label for="birthday">Your birthday:</label>
      <input type="date" id="birthday" name="birthday"><br><!--date,类似日历格式，可以直接填写年月日，也可日历填写-->
      <label for="wakeup">You want to wake up at:</label>
      <input type="time" id="wakeup" name="wakeup"><br><!--直接时间格式-->
      <label for="color">Your favorite color:</label>
      <input type="color" id="color" name="color"> <br><!--颜色按钮，很丰富-->
      <label for="mood">Your mood:</label>
      Bad <input type="range" min="0" max="100" step="5" value="50" id="mood" name="mood"> Good<br><!--进度条可以左右滑动-->
      <input type="submit" value="Submit!">	
    </form>
    