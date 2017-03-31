# CSS 分页实例 #
简单分页
如果你的网站有很多个页面，你就需要使用分页来为每个页面做导航。
以下实例演示了如何使用 HTML 和 CSS 来创建分页：
CSS 实例
ul.pagination {
    display: inline-block;
    padding: 0;
    margin: 0;
}

ul.pagination li {display: inline;}

ul.pagination li a {
    color: black;
    float: left;
    padding: 8px 16px;
    text-decoration: none;
}
## 点击及鼠标悬停分页样式 ##
« 1 2 3 4 5 6 7 »
如果点击当前页，可以使用 .active 来设置当期页样式，鼠标悬停可以使用 :hover 选择器来修改样式：
CSS 实例
ul.pagination li a.active {
    background-color: #4CAF50;
    color: white;
}

ul.pagination li a:hover:not(.active) {background-color: #ddd;}
## 圆角样式 ##
« 1 2 3 4 5 6 7 »
可以使用 border-radius 属性为选中的页码来添加圆角样式:
CSS 实例
ul.pagination li a {
    border-radius: 5px;
}

ul.pagination li a.active {
    border-radius: 5px;
}
## 鼠标悬停过渡效果 ##
« 1 2 3 4 5 6 7 »
我们可以通过添加 transition 属性来为鼠标移动到页码上时添加过渡效果 to the page links to create a transition effect on hover:
CSS 实例
ul.pagination li a {
    transition: background-color .3s;
}
## 圆角边框 ##
提示: 在第一个分页链接和最后一个分页链接添加圆角：
« 1 2 3 4 5 6 7 »
CSS 实例
.pagination li:first-child a {
    border-top-left-radius: 5px;
    border-bottom-left-radius: 5px;
}

.pagination li:last-child a {
    border-top-right-radius: 5px;
    border-bottom-right-radius: 5px;
}
## 分页字体大小 ##
« 1 2 3 4 5 6 7 »
我们可以使用 font-size 属性来设置分页的字体大小:
CSS 实例
ul.pagination li a {
    font-size: 22px;
}