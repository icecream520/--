//获取数据
 31             Ext.Ajax.request({
 32                 url: '/App_Ashx/Demo/Ajax.ashx',
 33                 method: 'post',
 34                 params: { id: 1 },
 35                 success: function (response, options) {
 36                     for (i in options) {
 37                         alert('options参数名称:' + i);
 38                         alert('options参数[' + i + ']的值：' + options[i]);
 39                     }
 40                     var responseJson = Ext.util.JSON.decode(response.responseText);
 41                     template.compile();
 42                     template.overwrite(panel.body, responseJson);
 43                 },
 44                 failure: function () {
 45                     alert('系统出错，请联系管理人员！');
 46                 }
 47             });