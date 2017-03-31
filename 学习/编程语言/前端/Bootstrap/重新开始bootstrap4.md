# Bootstrap 按钮 #
任何带有 class .btn 的元素都会继承圆角灰色按钮的默认外观。但是 Bootstrap 提供了一些选项来定义按钮的样式，具体如下表所示：
以下样式可用于<a>, <button>, 或 <input> 元素上：
类	描述	实例
.btn	为按钮添加基本样式	尝试一下
.btn-default	默认/标准按钮	尝试一下
.btn-primary	原始按钮样式（未被操作）	尝试一下
.btn-success	表示成功的动作	尝试一下
.btn-info	该样式可用于要弹出信息的按钮	尝试一下
.btn-warning	表示需要谨慎操作的按钮	尝试一下
.btn-danger	表示一个危险动作的按钮操作	尝试一下
.btn-link	让按钮看起来像个链接 (仍然保留按钮行为)	尝试一下
.btn-lg	制作一个大按钮	尝试一下
.btn-sm	制作一个小按钮	尝试一下
.btn-xs	制作一个超小按钮	尝试一下
.btn-block	块级按钮(拉伸至父元素100%的宽度)	尝试一下
.active	按钮被点击	尝试一下
.disabled	禁用按钮	尝试一下
<!-- 标准的按钮 -->
<button type="button" class="btn btn-default">默认按钮</button>
<!-- 提供额外的视觉效果，标识一组按钮中的原始动作 -->
<button type="button" class="btn btn-primary">原始按钮</button>
<!-- 表示一个成功的或积极的动作 -->
<button type="button" class="btn btn-success">成功按钮</button>
<!-- 信息警告消息的上下文按钮 -->
<button type="button" class="btn btn-info">信息按钮</button>
<!-- 表示应谨慎采取的动作 -->
<button type="button" class="btn btn-warning">警告按钮</button>
<!-- 表示一个危险的或潜在的负面动作 -->
<button type="button" class="btn btn-danger">危险按钮</button>
<!-- 并不强调是一个按钮，看起来像一个链接，但同时保持按钮的行为 -->
<button type="button" class="btn btn-link">链接按钮</button>

## 按钮大小 ##
下表列出了获得各种大小按钮的 class：
Class	描述
.btn-lg	这会让按钮看起来比较大。
.btn-sm	这会让按钮看起来比较小。
.btn-xs	这会让按钮看起来特别小。
.btn-block	这会创建块级的按钮，会横跨父元素的全部宽度。
下面的实例演示了上面所有的按钮 class：

## 禁用状态 ##
当您禁用一个按钮时，它的颜色会变淡 50%，并失去渐变。
下表列出了让按钮元素和锚元素呈禁用状态的 class：
元素	Class
按钮元素	添加 disabled 属性 到 <button> 按钮。
锚元素	添加 disabled class 到 <a> 按钮。
注意：该 class 只会改变 <a> 的外观，不会改变它的功能。在这里，您需要使用自定义的 JavaScript 来禁用链接。

# Bootstrap 图片 #
.img-rounded：添加 border-radius:6px 来获得图片圆角。
.img-circle：添加 border-radius:50% 来让整个图片变成圆形。
.img-thumbnail：添加一些内边距（padding）和一个灰色的边框。

<img> 类
以下类可用于任何图片中。
类	描述	实例
.img-rounded	为图片添加圆角 (IE8 不支持)	尝试一下
.img-circle	将图片变为圆形 (IE8 不支持)	尝试一下
.img-thumbnail	缩略图功能	尝试一下
.img-responsive	图片响应式 (将很好地扩展到父元素)	尝试一下

本章总结：首先就是button有很多样式 btn 及他各种延伸,还有图片图片有圆角的圆的有Padding做缩略图的还有img-responsive响应式