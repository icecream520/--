# CSS3 边框 #
## CSS3 边框 ##
用CSS3，你可以创建圆角边框，添加阴影框，并作为边界的形象而不使用设计程序，如Photoshop。
在本章中，您将了解以下的边框属性：
border-radius
box-shadow
border-image
## CSS3 圆角 ##
在CSS2中添加圆角棘手。我们不得不在每个角落使用不同的图像。
在CSS3中，很容易创建圆角。
在CSS3中border-radius属性被用于创建圆角：
这是圆角边框！
实例
在div中添加圆角元素：
div
{
border:2px solid;
border-radius:25px;
}
## CSS3盒阴影 ##
CSS3中的box-shadow属性被用来添加阴影:

实例
在div中添加box-shadow属性
div
{
box-shadow: 10px 10px 5px #888888;
}
## CSS3边界图片 ##
有了CSS3的border-image属性，你可以使用图像创建一个边框：
border-image属性允许你指定一个图片作为边框！ 用于创建上文边框的原始图像：
在div中使用图片创建边框:
Border

实例
在div中使用图片创建边框
div
{
border-image:url(border.png) 30 30 round;
-webkit-border-image:url(border.png) 30 30 round; /* Safari 5 and older */
-o-border-image:url(border.png) 30 30 round; /* Opera */
}