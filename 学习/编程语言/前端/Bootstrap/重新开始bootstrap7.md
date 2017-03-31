# Bootstrap 下拉菜单（Dropdowns） #
data-toggle
BS的自定义属性..关联BS的JS插件的....来实现下拉菜单
BS的下拉菜单设置宽度是只需要将 dropdown 的min-width: 改掉就可以
role是标签扮演的角色属性，更多的是注明作用，对css样式没影响。
presentation在这里表示陈述。

本章将重点介绍 Bootstrap 下拉菜单。下拉菜单是可切换的，是以列表格式显示链接的上下文菜单。这可以通过与 下拉菜单（Dropdown） JavaScript 插件 的互动来实现。
如需使用下列菜单，只需要在 class .dropdown 内加上下拉菜单即可。下面的实例演示了基本的下拉菜单：
<div class="dropdown">
    <button type="button" class="btn dropdown-toggle" id="dropdownMenu1" data-toggle="dropdown">主题
        <span class="caret"></span>
    </button>
    <ul class="dropdown-menu" role="menu" aria-labelledby="dropdownMenu1">
        <li role="presentation">
            <a role="menuitem" tabindex="-1" href="#">Java</a>
        </li>
        <li role="presentation">
            <a role="menuitem" tabindex="-1" href="#">数据挖掘</a>
        </li>
        <li role="presentation">
            <a role="menuitem" tabindex="-1" href="#">数据通信/网络</a>
        </li>
        <li role="presentation" class="divider"></li>
        <li role="presentation">
            <a role="menuitem" tabindex="-1" href="#">分离的链接</a>
        </li>
    </ul>
</div>

选项
对齐
通过向 .dropdown-menu 添加 class .pull-right 来向右对齐下拉菜单。下面的实例演示了这点：
### 标题 ###
您可以使用 class dropdown-header 向下拉菜单的标签区域添加标题。下面的实例演示了这点：

.dropdown	指定下拉菜单，下拉菜单都包裹在 .dropdown 里	尝试一下
.dropdown-menu	创建下拉菜单	尝试一下
.dropdown-menu-right	下拉菜单右对齐	尝试一下
.dropdown-header	下拉菜单中添加标题	尝试一下
.dropup	指定向上弹出的下拉菜单	尝试一下
.disabled	下拉菜单中的禁用项	尝试一下
.divider	下拉菜单中的分割线	尝试一下

# Bootstrap 按钮组 #
按钮组允许多个按钮被堆叠在同一行上。当你想要把按钮对齐在一起时，这就显得非常有用。您可以通过 Bootstrap 按钮（Button） 插件 添加可选的 JavaScript 单选框和复选框样式行为。
下面的表格总结了 Bootstrap 提供的使用按钮组的一些重要的 class：
Class	描述	代码示例
.btn-group	该 class 用于形成基本的按钮组。在 .btn-group 中放置一系列带有 class .btn 的按钮。	
<div class="btn-group">
  <button type="button" class="btn btn-default">Button1</button>
   <button type="button" class="btn btn-default">Button2</button>
</div>
.btn-toolbar	该 class 有助于把几组 <div class="btn-group"> 结合到一个 <div class="btn-toolbar"> 中，一般获得更复杂的组件。	
<div class="btn-toolbar" role="toolbar">
  <div class="btn-group">...</div>
  <div class="btn-group">...</div>
</div>
.btn-group-lg, .btn-group-sm, .btn-group-xs	这些 class 可应用到整个按钮组的大小调整，而不需要对每个按钮进行大小调整。	
<div class="btn-group btn-group-lg">...</div>
<div class="btn-group btn-group-sm">...</div>
<div class="btn-group btn-group-xs">...</div>
.btn-group-vertical	该 class 让一组按钮垂直堆叠显示，而不是水平堆叠显示。	
<div class="btn-group-vertical">
  ...
</div>
## 按钮工具栏 ##
下面的实例演示了上面表格中讨论到的 class .btn-toolbar 的使用：
<div class="btn-toolbar" role="toolbar">
<div class="btn-group">
    <button type="button" class="btn btn-default">按钮 1</button>
    <button type="button" class="btn btn-default">按钮 2</button>
    <button type="button" class="btn btn-default">按钮 3</button>
 </div>
<div class="btn-group">
    <button type="button" class="btn btn-default">按钮 4</button>
    <button type="button" class="btn btn-default">按钮 5</button>
    <button type="button" class="btn btn-default">按钮 6</button>
</div>
<div class="btn-group">
    <button type="button" class="btn btn-default">按钮 7</button>
    <button type="button" class="btn btn-default">按钮 8</button>
    <button type="button" class="btn btn-default">按钮 9</button>
</div>
</div>
## 按钮的大小 ##
下面的实例演示了上面表格中讨论到的 class .btn-group-* 的使用：
   <button type="button" class="btn btn-default">按钮 2</button>
    <button type="button" class="btn btn-default">按钮 3</button>
</div>
    <div class="btn-group btn-group-sm">
    <button type="button" class="btn btn-default">按钮 4</button>
    <button type="button" class="btn btn-default">按钮 5</button>
    <button type="button" class="btn btn-default">按钮 6</button>
</div>
    <div class="btn-group btn-group-xs">
    <button type="button" class="btn btn-default">按钮 7</button>
    <button type="button" class="btn btn-default">按钮 8</button>
    <button type="button" class="btn btn-default">按钮 9</button>
</div>
## 嵌套 ##
您可以在一个按钮组内嵌套另一个按钮组，即，在一个 .btn-group 内嵌套另一个 .btn-group 。当您向让下拉菜单与一系列按钮组合使用时，就会用到这个。
<div class="btn-group">
    <button type="button" class="btn btn-default">按钮 1</button>
    <button type="button" class="btn btn-default">按钮 2</button>
    <div class="btn-group">
    <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown">
        下列
        <span class="caret"></span>
    </button>
    <ul class="dropdown-menu">
        <li><a href="#">下拉链接 1</a></li>
        <li><a href="#">下拉链接 2</a></li>
    </ul>
    </div>
</div>

## 垂直的按钮组 ##
下面的实例演示了上面表格中讨论到的 class .btn-group-vertical 的使用
<div class="btn-group-vertical">
    <button type="button" class="btn btn-default">按钮 1</button>
    <button type="button" class="btn btn-default">按钮 2</button>
    <div class="btn-group-vertical">
    <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown">
        下拉
        <span class="caret"></span>
    </button>
    <ul class="dropdown-menu">
        <li><a href="#">下拉链接 1</a></li>
        <li><a href="#">下拉链接 2</a></li>
    </ul>
    </div>
</div>