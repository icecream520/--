ExtJS自定义类的 alias 里的字段含义?
extend : 'Ext.panel.Panel', alias : 'widget.v_georaecheodeungrok',
 
extend : 'Ext.app.ViewController', alias : 'controller.c_georaecheodeungrok',
 
extend : 'Ext.app.ViewModel', alias : 'viewmodel.m_georaecheodeungrok',
 
问题:
 
一个模块定义了三个类各继承自 panel, ViewController',  ViewModel',
 
我的疑问是, 后面 alias 属性里的 widget, controller, viewmodel 有特殊含义吗?
extjs5以后，增加了MVVM设计思想，就是在extjs4的mvc的基础上多了一个viewmodel
你提到的alias就是这个类的别名，别名的命名要遵守mvvm命名要求，要不然在使用的时候就会报错。
即view的别名用widget.XX  controller的别名用'controller.XX viewmodel
的别名用viewmodel.XX   

其中widget别名主要用于xtype:XX   controller和viewmdel就是在view做绑定的，不能写错的
希望对你有帮助，有问题可以再问我。