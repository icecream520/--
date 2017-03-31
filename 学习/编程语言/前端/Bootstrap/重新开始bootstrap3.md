# Bootstrap 表单 #
## 表单布局 ##
Bootstrap 提供了下列类型的表单布局：
垂直表单（默认）
内联表单
水平表单
垂直或基本表单
基本的表单结构是 Bootstrap 自带的，个别的表单控件自动接收一些全局样式。下面列出了创建基本表单的步骤：
向父 <form> 元素添加 role="form"。
把标签和控件放在一个带有 class .form-group 的 <div> 中。这是获取最佳间距所必需的。
向所有的文本元素 <input>、<textarea> 和 <select> 添加 class .form-control。
## 内联表单 ##
如果需要创建一个表单，它的所有元素是内联的，向左对齐的，标签是并排的，请向 <form> 标签添加 class .form-inline。
class="form-group" 获取最佳间距
内联表单
<form>class添加 form-inline
## 水平表单 ##
水平表单与其他表单不仅标记的数量上不同，而且表单的呈现形式也不同。如需创建一个水平布局的表单，请按下面的几个步骤进行：
向父 <form> 元素添加 class .form-horizontal。
把标签和控件放在一个带有 class .form-group 的 <div> 中。
向标签添加 class .control-label.在BootStrap默认情况下它的文本采用右对齐方式。一个小的label
## 支持的表单控件 ##
Bootstrap 支持最常见的表单控件，主要是 input、textarea、checkbox、radio 和 select。
输入框（Input）
最常见的表单文本字段是输入框 input。用户可以在其中输入大多数必要的表单数据。Bootstrap 提供了对所有原生的 HTML5 的 input 类型的支持，包括：text、password、datetime、datetime-local、date、month、time、week、number、email、url、search、tel 和 color。适当的 type 声明是必需的，这样才能让 input 获得完整的样式。
<form role="form">
  <div class="form-group">
    <label for="name">标签</label>
    <input type="text" class="form-control" placeholder="文本输入">
  </div>
 </form>
placeholder="文本输入"就是说form表单的内部提示

## 文本框（Textarea） ##
当您需要进行多行输入的时，则可以使用文本框 textarea。必要时可以改变 rows 属性（较少的行 = 较小的盒子，较多的行 = 较大的盒子）。
实例
<form role="form">
  <div class="form-group">
    <label for="name">文本框</label>
    <textarea class="form-control" rows="3"></textarea>
  </div>
</form>
form-control:就是全屏框

## 复选框（Checkbox）和单选框（Radio） ##
复选框和单选按钮用于让用户从一系列预设置的选项中进行选择。
当创建表单时，如果您想让用户从列表中选择若干个选项时，请使用 checkbox。如果您限制用户只能选择一个选项，请使用 radio。
对一系列复选框和单选框使用 .checkbox-inline 或 .radio-inline class，控制它们显示在同一行上。
下面的实例演示了这两种类型（默认和内联）：

## 选择框（Select） ##
当您想让用户从多个选项中进行选择，但是默认情况下只能选择一个选项时，则使用选择框。
使用 <select> 展示列表选项，通常是那些用户很熟悉的选择列表，比如州或者数字。
使用 multiple="multiple" 允许用户选择多个选项。

## 静态控件 ##
当您需要在一个水平表单内的表单标签后放置纯文本时，请在 <p> 上使用 class .form-control-static。
不是不是静态控件竟然对不齐？
.form-control-static {
  min-height: 34px;
  padding-top: 7px;
  padding-bottom: 7px;
  margin-bottom: 0;
}

## 表单控件状态 ##
除了 :focus 状态（即，用户点击 input 或使用 tab 键聚焦到 input 上），Bootstrap 还为禁用的输入框定义了样式，并提供了表单验证的 class。
输入框焦点
当输入框 input 接收到 :focus 时，输入框的轮廓会被移除，同时应用 box-shadow。
禁用的输入框 input
如果您想要禁用一个输入框 input，只需要简单地添加 disabled 属性，这不仅会禁用输入框，还会改变输入框的样式以及当鼠标的指针悬停在元素上时鼠标指针的样式。
禁用的字段集 fieldset
对 <fieldset> 添加 disabled 属性来禁用 <fieldset> 内的所有控件。
验证状态
Bootstrap 包含了错误、警告和成功消息的验证样式。只需要对父元素简单地添加适当的 class（.has-warning、 .has-error 或 .has-success）即可使用验证状态。
下面的实例演示了所有控件状态：


## 表单控件大小 ##
您可以分别使用 class .input-lg 和 .col-lg-* 来设置表单的高度和宽度。下面的实例演示了这点：
## 表单帮助文本 ##
Bootstrap 表单控件可以在输入框 input 上有一个块级帮助文本。为了添加一个占用整个宽度的内容块，请在 <input> 后使用 .help-block
本节内容:
表单控件介绍,包括from-group成块结构 <form role="form"> 要是内联添加form-inline 水平 form-horizontal 表达禁止输入disabled
 <div class="form-group">
    <label for="inputPassword" class="col-sm-2 control-label">禁用</label>
    <div class="col-sm-10">
      <input class="form-control" id="disabledInput" type="text" placeholder="该输入框禁止输入..." disabled>
    </div>
  </div>
  <fieldset disabled>
    <div class="form-group">
      <label for="disabledTextInput" class="col-sm-2 control-label">禁用输入（Fieldset disabled）</label>
      <div class="col-sm-10">
        <input type="text" id="disabledTextInput" class="form-control" placeholder="禁止输入">
      </div>
    </div>
    <div class="form-group">
      <label for="disabledSelect" class="col-sm-2 control-label">禁用选择菜单（Fieldset disabled）</label>
      <div class="col-sm-10">
        <select id="disabledSelect" class="form-control">
          <option>禁止选择</option>
        </select>
      </div>
    </div>
  </fieldset>

<fieldset disabled>这个是里面的所有控件都不能输入
表单控件大小控制class input-lg col-lg第一个是在<input class="">里面添加第二个是div添加