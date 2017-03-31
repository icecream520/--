View  Bag 允许在一个动态的对象上定义任意属性,并在视图中访问它.这个动态的对象可以通过Controller.ViewBag属性访问它.
@RenderBody（）:呈现子页的主体内容

　　@RenderSection（）：呈现特别的节部分。

　　HelperResult RenderSection(string name, bool required = true);

　　required默认为true必须覆写，设为false则为可选覆写；

　　注意的是：该函数在RC版中参数有所改变，参数中optional改为required，据说和VB的关键字冲突

　　下图则为我在子页的页脚部分覆写，在子页实现时，使用@section 自定义节名{ }格式。
