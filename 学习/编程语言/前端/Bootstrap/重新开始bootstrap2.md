# Bootstrap 代码 #
Bootstrap 允许您以两种方式显示代码：
第一种是 <code> 标签。如果您想要内联显示代码，那么您应该使用 <code> 标签。
第二种是 <pre> 标签。如果代码需要被显示为一个独立的块元素或者代码有多行，那么您应该使用 <pre> 标签。
请确保当您使用 <pre> 和 <code> 标签时，开始和结束标签使用了 unicode 变体： &lt; 和 &gt;。
让我们来看看下面的实例：
实例
<p><code>&lt;header&gt;</code> 作为内联元素被包围。</p>
<p>如果需要把代码显示为一个独立的块元素，请使用 &lt;pre&gt; 标签：</p>
<pre>
    &lt;article&gt;
        &lt;h1&gt;Article Heading&lt;/h1&gt;
    &lt;/article&gt;
</pre>

## 更多实例 ##
元素/类	描述	实例
<var>	变量赋值: x = ab + y	尝试一下
<kbd>	按键提示： CTRL + P	尝试一下
<pre>	多行代码	尝试一下
<pre class="pre-scrollable">	多行代码带有滚动条	尝试一下
<samp>	电脑程序输出: Sample output	尝试一下
<code>	同一行代码片段: span, div

以后每看完一章就要总结:
<code>显示代码代码内联</code>
<pre>显示代码代码块</pre>
<pre class="pre-scrollable">显示代码块,并且块有大小改为通过上下条来拉动</pre>
<kbd>按键提示</kbd>
 开始标签&lt; 和 结束标签&gt;
&lt,&gt

# Bootstrap 表格 #
bootstrap3中container与container_fluid容器的区别
.container 类用于固定宽度并支持响应式布局的容器。

.container-fluid 类用于 100% 宽度，占据全部视口（viewport）的容器。

Bootstrap 提供了一个清晰的创建表格的布局。下表列出了 Bootstrap 支持的一些表格元素：
标签	描述
<table>	为表格添加基础样式。
<thead>	表格标题行的容器元素（<tr>），用来标识表格列。
<tbody>	表格主体中的表格行的容器元素（<tr>）。
<tr>	一组出现在单行上的表格单元格的容器元素（<td> 或 <th>）。
<td>	默认的表格单元格。
<th>	特殊的表格单元格，用来标识列或行（取决于范围和位置）。必须在 <thead> 内使用。
<caption>	关于表格存储内容的描述或总结。
## 表格类 ##
下表样式可用于表格中：
类	描述	实例
.table	为任意 <table> 添加基本样式 (只有横向分隔线)	尝试一下
.table-striped	在 <tbody> 内添加斑马线形式的条纹 ( IE8 不支持)	尝试一下 //斑马线条纹就是有颜色没有颜色
.table-bordered	为所有表格的单元格添加边框	尝试一下
.table-hover	在 <tbody> 内的任一行启用鼠标悬停状态	尝试一下
.table-condensed	让表格更加紧凑	尝试一下
联合使用所有表格类	尝试一下

	<table class="table">
		<thead>
			<tr>
				<th>#</th>
				<th>Firstname</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>1</td>
				<td>Anna</td>
			</tr>
			<tr>
				<td>2</td>
				<td>Debbie</td>
			</tr>
			<tr>
				<td>3</td>
				<td>John</td>
			</tr>
		</tbody>
	</table>

	<table class="table table-striped">
		<thead>
			<tr>
				<th>#</th>
				<th>Firstname</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>1</td>
				<td>Anna</td>
			</tr>
			<tr>
				<td>2</td>
				<td>Debbie</td>
			</tr>
			<tr>
				<td>3</td>
				<td>John</td>
			</tr>
		</tbody>
	</table>

<tr>, <th> 和 <td> 类
下表的类可用于表格的行或者单元格：
类	描述	实例
.active	将悬停的颜色应用在行或者单元格上	尝试一下
.success	表示成功的操作	尝试一下
.info	表示信息变化的操作	尝试一下
.warning	表示一个警告的操作	尝试一下
.danger	表示一个危险的操作

悬停表格
通过添加 .table-hover class，当指针悬停在行上时会出现浅灰色背景。
## 上下文类 ##
下表中所列出的上下文类允许您改变表格行或单个单元格的背景颜色。
类	描述
.active	对某一特定的行或单元格应用悬停颜色
.success	表示一个成功的或积极的动作
.warning	表示一个需要注意的警告
.danger	表示一个危险的或潜在的负面动作
## 响应式表格 ##
通过把任意的 .table 包在 .table-responsive class 内，您可以让表格水平滚动以适应小型设备（小于 768px）。当在大于 768px 宽的大型设备上查看时，您将看不到任何的差别。

本章总结
<table>
<thead>
<tr>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
</tr>
</tbody>
</table>
class类：table类给table增加些默认样式
table-hover:鼠标悬停时增加灰色背景
table-bordered:table增加边框
还有一些给表格增加颜色的警告什么的