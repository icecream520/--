 Extjs4中up()和down()的用法
Extjs4.x中，每个组件都新增加了两个方法up()和down()方法。这两个方法都是用来获取组件的，下面我们来看下up()方法和down()方法的官方解释。
Extjs4.x中，新增加了两个方法up()和down()方法。这两个方法都是用来获取组件的，下面我们来看下官方解释。
up( String selector, [Number/Mixed maxDepth] ) : Ext.core.Element
selector:必选，字符串形式，表示要匹配的组件。
Maxdepth:可选，表示要匹配的最大深度。
up方法的API解释为：通过简单的选择，获得相匹配的dom，使用up方法总是返回一个Ext.core.Element，也就是ext的组件。
down( String selector, [Boolean returnDom] ) : HTMLElement/Ext.core.Element
selector:必选，字符串形式，表示要匹配的组件，
returnDom：可选，布尔类型，如果为true，则返回DOM节点，而不是Ext.core.Element。值默认为false。
down方法的API解释，通过选择器,来获得任何深度的子组件，在down方法中，不应该包含组件的id，而应该是组件的xtype。
下面我们来看他的用法。先看一段代码。
     
    Ext.require('Ext.*');
     Ext.onReady(function(){
      var win = Ext.create('Ext.window.Window',{
       height: 160,
       width: 280,
       title: '用户登陆',
       closeAction: 'hide',
       closable : false, 
       iconCls: 'win',
       layout: 'fit',
       modal : true, 
       plain : true,
       resizable: false,
       items:[{
    xtype:'form',
    items:[{
     //..... 
    }],
    button:[{
     text:'登录',
     handler:function(){
      
     }
    }]
       }]
      }) 
     });
    Ext.require('Ext.*');
     Ext.onReady(function(){
      var win = Ext.create('Ext.window.Window',{
       height: 160,
       width: 280,
       title: '用户登陆',
       closeAction: 'hide',
       closable : false, 
       iconCls: 'win',
       layout: 'fit',
       modal : true, 
       plain : true,
       resizable: false,
       items:[{
    xtype:'form',
    items:[{
     //..... 
    }],
    button:[{
     text:'登录',
     handler:function(){
      
     }
    }]
       }]
      }) 
     });

这段代码中，我们创建了一个window，然后在window中添加了一个form。最后增加了一个button。button的handler，我们定义了一个function。下一步，我们在这个function中添加代码。
 
var form = this.up(‘form’).getForm();
var form = this.up(‘form’).getForm();
这里用到了this.up。具体解释下。这里this。就是button组件，up(‘form’)是指匹配form组件。那么合起来，我们就得到了form组件，并且得到整个form。
在这个例子中，我们并不需要down方法。因为无论是获取form还是window.我们都可以使用this.up(‘form’)或this.up(‘window’)来获取form组件和window组件。
为了介绍下down方法。我们将整个过程复杂化一些。
 
var form = this.up(‘window’).down(‘form’).getForm();
var form = this.up(‘window’).down(‘form’).getForm();
相信大家已经很明白了,this.up(‘window’)获取了顶级的window组件。接着使用down()方法获取了window的子组件form组件，最后使用getForm()来获取整个form。
结语：在extjs4中，extjs给每个组件增加了up()和down()方法，这样使得我们更加容易得到每个组件的父级组件和子级组件。当然，除了这些方法，extjs还增加了更加强大的ComponentQuery类，通过这个类，我们可以使用更多的方法来找到所需要的任何组件。具体ComponentQuery的用法