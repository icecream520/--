# 数据存储 Stroe #
## Record ##
首先需要明确是， ExtJS中有一个名为Record的类， 表格等控件中使用的数据是存放在
Record对象中，一个Record可以理解为关系数据表中的一行，也可以称为记录。 Record对
象中即包含了记录（行中各列）的定义信息（也就是该记录包含哪些字段，每一个字段的
据类型等） ，同时又包含了记录具体的数据信息（也就是各个字段的值） 

## Store ##
  Store可以理解为数据存储器，可以理解为客户端的小型数据表，提供缓存等功能。在
ExtJS中， GridPanel、 ComboBox、 DataView等控件一般直接与Store打交道， 直接通过store
来获得控件中需要展现的数据等。一个Store包含多个Record，同时Store又包含了数据来
源，数据解析器等相关信息， Store通过调用具体的数据解析器(DataReader)来解析指定类型
或格式的数据(DataProxy)，并转换成记录集的形式保存在Store中，作为其它控件的数据输入。
  数据存储器由Ext.data.Store类定义，一个完整的数据存储器要知道数据源(DataProxy)
及数据解析方式(DataReader)才能工作， 在Ext.data.Store类中数据源由proxy配置属性定义、
数据解析（读取）器由reader配置属性定义，一个较为按部就班创建Store的代码如下