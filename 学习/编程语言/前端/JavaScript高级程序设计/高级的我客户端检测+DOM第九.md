由于浏览器存在差别,通常需要根据不同的浏览器能力编写不同的代码
1:能力检测  
2:怪癖检测
3:用户代理检测


# DOM #
 文档节点每个文档的根节点,文档元素是文档最外层的元素，文档中其他所有元素都包含在文档元素中.
每个节点都有一个childNodes属性,其中保存着一个NodeList对象，NodeList是一种类数组对象，用于保存一组有序的节点，可以通过为止来访问这些节点。
可以通过方括号预防来访问NodeList的值,对象而又length属性,但它并不是Array的实例。
访问NodeList中的节点
someNode.childNodes[0];
someNode.childNodes.item(1);

对 arguments对象使用Array.prototype.slice()方法可以将其转换为数组。

var arrayOfNodes = Array.prototype.slice.call(someNode.childNodes,0);


每个节点都有一个parentNode属性,该属性指向文档树种的父节点。通过使用列表中的每个节点的previousSibling和nextSibling属性，可以访问同一列表中的最近的节点。
所有节点都有最后一个属性时ownerDocument该属性指向整个文档的文档节点。

## 操作节点 ##

appendChild()用于向childNodes列表末尾添加一个节点。
如果需要把节点放在列表中某个特定的位置上而不是放在末尾,那么可以使用insertBefore()方法。接收两个参数要插入的节点和作为参照的节点。
在插入的参照节点之前该节点。
replaceChild(),插入一个节点。
removeChild()移除一个节点
### 其他方法 ###
cloneNode(),此方法接收一个Bool参数表示是否要执行深复制，ture的时候复制节点及其整个子节点数,在为false情况下,执行浅复制,值复制节点本身,复制后返回的及诶单副本属于文档所有,并没有指定父节点。


### Document类型 ###
document对象是HTMLDocument的一个实例,表示整个HTML页面。

URL,domain,referrer

URL属性中包含页面完整的URL,domain属性中只包含页面的域名,referrer属性则是保存着链接到当前页面的的那个页面的URL.
不能将domain设置成URL中不包含的域。
域名一开始是松散的,就不能再将它设置成紧绷的。

### 查找元素 ###
getElementById(),getElementByTagName();//TagName标签名

### 文档写入 ###
将输入流写入到网页中,动态的包含外部资源。

### Element类型 ###
元素中指定的所有信息,都可以通过下列js实现
var div =document.grtElementByid("id");
alert(div.id);//元素在文档中的唯一标识符。
alert(div.className);//与元素class特性对应
alert(div.title);//有关元素的附加说明信息
alert(div.dir);//语言方向ltr，=left to right
也可以通过.语法给每个属性赋予新的值。
### 取得特性 ###
特性的用户时给出相应元素或其内容的附加信息。
操作特性DOM方法主要有三个getAttribute()、setAttribute()、removeAttribute().
getAttribute也可以取得自定义的特性

### 设置特性 ###
setAttribute(),这个方法接收两个参数，要设置的特性名和值。
例
div.setAttribute("id","someOtherID");
通过这个方法设置的特性名会被统一转换为小写形式,即ID变成id

removeAttribute()这个方法用于彻底删除元素的特性。不仅会清除特性的值,而且也会从元素中完全删除特性。
