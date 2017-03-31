jQuery表单验证插件 validation  validate 验证 directory 目录 repository 知识库

<script src="lib/jquery.validate.js" type="text/javascript"></script>//引入jquery

$("#commentForm").validate({meta: "validate"});//验证哪个表单需要验证

class="required"必填 minlength="2" 最短长度为2
class="required email"
class="url"

有什么？表单提交的时候需要必填，格式等，然后转换成中文，错误提示信息自己写，然后图像错的，对的，有个没有遵守规则的标签，然后有验证码

jQuery表单插件 ————form
就是将表单数据结构化，然后方便ajax提交方式。Ajax方式提交的话非常方便，不用整个页面提交，只需要相应的页面提交就好了