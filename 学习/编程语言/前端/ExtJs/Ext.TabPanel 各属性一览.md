#  Ext.TabPanel 各属性一览 #
1、主要配置项：
      activeTab：初始激活的tab，索引或者id值，默认为none
 
      autoTabs：是否自动将带有'x-tab'样式类的div转成tabs添加到TabPanel中，默认为false。
            当该配置项设为true时，需要设置deferredRender为false，还必须使用applyTo。
      deferredRender：是否延迟渲染，默认为true。
      autoTabSelector：默认为'div.x-tab'。
 
      resizeTabs：是否可以改变tab的尺寸，默认为false。
      minTabWidth：tab的最小宽度，默认为30。
      tabWidth：每个新增加的tab宽度，默认为120。
      tabTip：tab的提示信息
 
      tabPosition：tab位置，可选值有top、bottom，默认为top。
      enableTabScroll：是否允许Tab溢出时可以滚动，默认为false。
      closable：tab是否可关闭，默认为false
 
      scrollDuration：每次的滚动时长，默认为0.35毫秒。
      scrollIncrement：每次的滚动步长，默认为100像素。
      wheelIncrement：每次鼠标滑轮的滚动步长，默认为20像素。
 
2、主要方法：
      activate( String/Panel tab )
      getActiveTab()：获取当前活动的tab
      get( String/Number key )：根据组件id或者索引获取组件
      getItem(String id)：根据tab id获取tab
      setActiveTab( String/Number item )
      remove( Component/String component, [Boolean autoDestroy] )
      removeAll( [Boolean autoDestroy] )

3、范例
new Ext.TabPanel({
id: "mainTab",
renderTo: "div1",
width: 500,
height: 300,
activeTab: 0,
defaults: {
autoScroll: true,
autoHeight:true,
style: "padding:5"
},
items:[
{title:"normal", tabTip:"mormal", html:"tab1", iconCls:"add"},
{title:"ajax1", autoLoad:"messagebox.action", iconCls:"delete"},
{title:"ajax2", autoLoad:{url:"test.action", params:"p1=v1", nocache:true}, iconCls:"search"},
{title:"event", iconCls:"save", listeners:{activate:activateHandler}}
],
enableTabScroll: true
});

function activateHandler(tab){
//alert(tab.title);
}

var index = 0;
function addTab(){
var tabs = Ext.getCmp("mainTab");
var t = tabs.getItem("tab"+index);
if(t) tabs.remove(t);
tabs.add({
id: "tab" + (++index),
title: "NewTab" + index,
html: "new tab" + index,
closable: true
}).show();
}

//按钮渲染到div1元素之前
new Ext.Button({
text:"add tab",
handler:addTab,
iconCls:"add"
}).render(document.body, "div1");

在使用TabPanel时需要注意：
       1、在创建Ext.TabPanel时deferredRender配置项经常会被忽略。该配置项的默认值是true。true表示只有在用户第一次访问选项卡时，该选项卡的panel才会被渲染。 所以当我们有可能使用脚本操作选项卡时，谨记将该配置项设置为false。
 
       2、在FormPanel中使用TabPanel，如果在TabPanel中不定义deferredRender的值为false，那么，当你使用Load方法为Form加载数据，或使用setValue为没有激活过的Panel的控件赋值时，将会发生错误。原因是，在默认设置下deferredRender为true，TabPanel并不会渲染所有Panel上的控件，只有在该Panel被激活时才渲染控件，所以当你为这些控件设置数据时，将会找不到这些控件，会出现错误。因而，在FormPanel中使用TabPanel，一定要在TabPanel中设置deferredRender的值为false，强制TabPanel在Layout渲染时同时渲染所有Panel上的控件。

来源： http://chenjumin.javaeye.com/blog/670734#