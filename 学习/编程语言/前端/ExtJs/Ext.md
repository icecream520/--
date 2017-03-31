 http://localhost:1841 部署的站点
下载一个4.多的版本，然后直接iis部署
Model间有两种关系
belongsTo：多对一关系
hasMany:一对多关系
作者 书 章节 作者一对多书 书多对一作者
Model：
Ext.define('Author'){
         extend:'Ext.data.Model'
         fields:[
         {name:'id',type:'int'},
         {name:'name',type:'string'},
],
       hasMany:{model:'Book',foreignKey:'authorId'},
       proxy:{
            type:'ajax',
            url:'../../Scripts/Test/author.js'
}
}
组件可分为三大类：基本组件，工具栏组件，表单及元素组件。
## 布局 ##
### Border 布局 ###
Border 布局由类Ext.layout.BorderLayout定义，布局名称为border,该布局把容器分为东南西北中五个区域
Ext.onReady(function(){
  new Ext.Viewport({
  layout:"border",
  items:[{region:"north",
  height:50,
  title:"顶部面板"},
  {region:"south",
  height:50,
  title:"底部面板"},
 {region:"center",
 title:"中央面板"},
 {region:"west",
 width:100,
 title:"左边面板"},
 {region:"east",
 width:100,
 title:"右边面板"}
 ]
});
});

### Column 列布局 ###
Column 列布局由Ext.layout.ColumnLayout 类定义，名称为column。列布局把整个容器
组件看成一列，然后往里面放入子元素的时候，可以通过在子元素中指定使用columnWidth
或width 来指定子元素所占的列宽度。columnWidth 表示使用百分比的形式指定列宽度，而
width 则是使用绝对象素的方式指定列宽度，在实际应用中可以混合使用两种方式。看下面
的代码：
Ext.onReady(function(){
   new Ext.Panel({
   renderTo:"hello",
   title:"容器组件",
   layout:"column",
   width:500,
   height:100,
   items:[{title:"列1",width:100},
{title:"列2",width:200},
{title:"列3",width:100},
{title:"列4"}
]
}
);
});
### Fit 布局 ###
自动填充满
如果容器组件中有多个子元素，则只会显示一个元素，如下面的代码：
Ext.onReady(function(){
   new Ext.Panel({
   renderTo:"hello",
   title:"容器组件",
   layout:"fit",
   width:500,
   height:100,
   items:[{title:"子元素1",html:"这是子元素1中的内容"},
{title:"子元素2",html:"这是子元素2中的内容"}
] }
);
});
Ext.onReady(function(){
  new Ext.Panel({
  renderTo:"hello",
  title:"容器组件",
  width:500,
  height:120,
  items:[{title:"子元素1",html:"这是子元素1中的内容"},
{title:"子元素2",html:"这是子元素2中的内容"}
] }
);
});
## Form布局 ##
Form布局由类Ext.layout.FormLayout定义，名称为form，是一种专门用于管理表单中
输入字段的布局， 这种布局主要用于在程序中创建表单字段或表单元素等使用。 看下面的代
码
Ext.onReady(function(){
  newExt.Panel({
  renderTo:"hello",
  title:"容器组件",
  width:300,
  layout:"form",
  hideLabels:false,
  labelAlign:"right"
  eight:120,
  defaultType:'textfield',
  items:[
{fieldLabel:"请输入姓名",name:"name"},
{fieldLabel:"请输入地址",name:"address"},
{fieldLabel:"请输入电话",name:"tel"}
]}
);
});

items:[{title:"子元素1",html:"这是子元素1中的内容",rowspan:2,height:100},//row行跨两行单元格
{title:"子元素2",html:"这是子元素2中的内容",colspan:2},//colspan列跨两行单元格
{title:"子元素3",html:"这是子元素3中的内容"},
{title:"子元素4",html:"这是子元素4中的内容"}。

onload,与Ext.onReady,第一个等全部资源加载完毕进行操作，第二个等DOM加载完成之后进行操作