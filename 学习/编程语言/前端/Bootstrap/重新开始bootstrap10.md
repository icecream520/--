# Bootstrap 导航元素 #
本章我们将讲解 Bootstrap 提供的用于定义导航元素的一些选项。它们使用相同的标记和基类 .nav。Bootstrap 也提供了一个用于共享标记和状态的帮助器类。改变修饰的 class，可以在不同的样式间进行切换。
## 表格导航或标签 ##
创建一个标签式的导航菜单：
以一个带有 class .nav 的无序列表开始。
添加 class .nav-tabs。
下面的实例演示了这点：
<p>标签式的导航菜单</p>
<ul class="nav nav-tabs">
  <li class="active"><a href="#">Home</a></li>
  <li><a href="#">SVN</a></li>
  <li><a href="#">iOS</a></li>
  <li><a href="#">VB.Net</a></li>
  <li><a href="#">Java</a></li>
  <li><a href="#">PHP</a></li>
</ul>
## 胶囊式的导航菜单 ##
基本的胶囊式导航菜单
如果需要把标签改成胶囊的样式，只需要使用 class .nav-pills 代替 .nav-tabs 即可，其他的步骤与上面相同。
下面的实例演示了这点：

## 垂直的胶囊式导航菜单 ##
您可以在使用 class .nav、.nav-pills 的同时使用 class .nav-stacked，让胶囊垂直堆叠。
下面的实例演示了这点：

## 两端对齐的导航 ##
您可以在屏幕宽度大于 768px 时，通过在分别使用 .nav、.nav-tabs 或 .nav、.nav-pills 的同时使用 class .nav-justified，让标签式或胶囊式导航菜单与父元素等宽。在更小的屏幕上，导航链接会堆叠。
下面的实例演示了这点：

## 禁用链接 ##
对每个 .nav class，如果添加了 .disabled class，则会创建一个灰色的链接，同时禁用了该链接的 :hover 状态，如下面的实例所示：
该 class 只会改变 <a> 的外观，不会改变它的功能。在这里，您需要使用自定义的 JavaScript 来禁用链接
## 下拉菜单 ##
导航菜单与下拉菜单使用相似的语法。默认情况下，列表项的锚与一些数据属性协同合作来触发带有 .dropdown-menu class 的无序列表。
带有下拉菜单的标签
向标签添加下拉菜单的步骤如下：
以一个带有 class .nav 的无序列表开始。
添加 class .nav-tabs。
添加带有 .dropdown-menu class 的无序列表。
## 更多导航元素组件实例 ##
标签页与胶囊式标签页
类	描述	实例
.nav nav-tabs	标签页	尝试一下
.nav nav-pills	胶囊式标签页	尝试一下
.nav nav-pills nav-stacked	胶囊式标签页以垂直方向堆叠排列的	尝试一下
.nav-justified	两端对齐的标签页，在大于 768px 的屏幕上，通过 .nav-justified 类可以很容易的让标签页或胶囊式标签呈现出同等宽度。在小屏幕上，导航链接呈现堆叠样式。	尝试一下
.disabled	禁用的标签页	尝试一下
标签添加下拉菜单	尝试一下
带下拉菜单的胶囊式标签页	尝试一下
.tab-content	与 .tab-pane 和 data-toggle="tab" (data-toggle="pill" ) 一同使用, 设置标签页对应的内容随标签的切换而更改	尝试一下
.tab-pane	与 .tab-content 和 data-toggle="tab" (data-toggle="pill")一同使用, 设置标签页对应的内容随标签的切换而更改

# Bootstrap 导航栏 #
导航栏是一个很好的功能，是 Bootstrap 网站的一个突出特点。导航栏在您的应用或网站中作为导航页头的响应式基础组件。导航栏在移动设备的视图中是折叠的，随着可用视口宽度的增加，导航栏也会水平展开。在 Bootstrap 导航栏的核心中，导航栏包括了站点名称和基本的导航定义样式。
## 默认的导航栏 ##
创建一个默认的导航栏的步骤如下：
向 <nav> 标签添加 class .navbar、.navbar-default。
向上面的元素添加 role="navigation"，有助于增加可访问性。
向 <div> 元素添加一个标题 class .navbar-header，内部包含了带有 class navbar-brand 的 <a> 元素。这会让文本看起来更大一号。
为了向导航栏添加链接，只需要简单地添加带有 class .nav、.navbar-nav 的无序列表即可。
<nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
    <div class="navbar-header">
        <a class="navbar-brand" href="#">菜鸟教程</a>
    </div>
    <div>
        <ul class="nav navbar-nav">
            <li class="active"><a href="#">iOS</a></li>
            <li><a href="#">SVN</a></li>
            <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown">
                    Java
                    <b class="caret"></b>
                </a>
                <ul class="dropdown-menu">
                    <li><a href="#">jmeter</a></li>
                    <li><a href="#">EJB</a></li>
                    <li><a href="#">Jasper Report</a></li>
                    <li class="divider"></li>
                    <li><a href="#">分离的链接</a></li>
                    <li class="divider"></li>
                    <li><a href="#">另一个分离的链接</a></li>
                </ul>
            </li>
        </ul>
    </div>
    </div>
</nav>