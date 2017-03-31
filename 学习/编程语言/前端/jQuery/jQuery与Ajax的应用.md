Ajax核心是XMLHttpRequest

## Ajax load方法 ##
load()方法是jQuery中能载入远程HTML代码并插入DOM中。
结构为
load(url [, data] [, callback]);
参数名字  类型     说明 
url     String   请求HTML页面的URL地址
data(可选) Object 发送至服务器的key/value数据
callback(可选) Function 请求完成时的回调函数，无论请求成功或失败

load()方法的传递方式是根据参数data来自动指定的，如果没有参数传递则采用Get方式传递，如果有则自动转换为Post方式。

  $("#resText").load("test.html .para",function (responseText, textStatus, XMLHttpRequest){
						 alert( $(this).html() );	//在这里this指向的是当前的DOM对象，即 $("#iptText")[0]
						 alert(responseText);       //请求返回的内容，整个html页面
						 alert(textStatus);		    //请求状态：success，error
						 alert(XMLHttpRequest);     //XMLHttpRequest对象
			});

$("#resText").html(data); // 把返回的数据添加到页面上
$("#resText").load(test.html); // 加载html代码
//两者的差别是,html是数据什么的插入，load是整html代码

load方法带不带参数可以判断选择哪种方式传输数据。

json数据格式 {\"key\",\"value\"};

## 动态创建Script ##
   $(function(){
        $('#send').click(function() {
             $.getScript('test.js');
        });
   })

## $.ajax(); ##

$.ajax(option)

## 序列化元素 ##
serialize()方法也是作用于jQuery对象，它能够将DOM元素内容序列化为字符串

serializeArray(),该方法不返回字符串，而是将DOM元素序列化后，返回json格式

$.param();用来对一个数组或对象按照key/value序列化

## 网页请求时提示信息 ##
  <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title></title>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<style type="text/css">
* { margin:0; padding:0;}
body { font-size:12px;}
#loading{
    width:80px;
	height: 20px;
	background:#bbb;
	color:#000;
	display:none;
}
img{border:0;height:100px;width:100px;}
.comment { margin-top:10px; padding:10px; border:1px solid #ccc;background:#DDD;}
.comment h6 { font-weight:700; font-size:14px;}
.para { margin-top:5px; text-indent:2em;background:#DDD;}
</style>
 <!--   引入jQuery -->
<script src="../scripts/jquery.js" type="text/javascript"></script>
<script type="text/javascript">
//<![CDATA[
   $(function(){
    //demo1:
        $('#send1').click(function() {
            $.getJSON("http://api.flickr.com/services/feeds/photos_public.gne?tags=car&tagmode=any&format=json&jsoncallback=?",
					  function(data){
					      $("#resText1").empty();
						  $.each(data.items, function( i,item ){
								$("<img/> ").attr("src", item.media.m ).appendTo("#resText1");
								if ( i == 3 ) { 
									return false;
								}
					      });
		             }
		    ); 
       });

   //demo2:
	   $("#send2").click(function(){
			$.get("get1.php", { 
						username :  $("#username").val() , 
						content :  $("#content").val()  
					}, function (data, textStatus){
                        $("#resText2").html(data); // 把返回的数据添加到页面上
					}
			);
	   })

		$.ajaxPrefilter(function( options ) {
			options.global = true;
		});
		//共用这2个全局的ajax事件
	   $("#loading").ajaxStart(function(){
	      $(this).show();
	   });
	   $("#loading").ajaxStop(function(){
	      $(this).hide();
	   });


   })
//]]>
</script>
</head>
<body>
<br/>
<div id="loading">加载中...</div>

<br/>
Demo1:
<br/>
<input type="button" id="send1" value="加载"/>
<div id="resText1" ></div>


<br/>
Demo2:
<br/>
<form id="form1" action="#">
<p>评论:</p>
 <p>姓名: <input type="text" name="username" id="username" /></p>
 <p>内容: <textarea name="content" id="content"  rows="2" cols="20"></textarea></p>
 <p><input type="button" id="send2" value="提交"/></p>
</form>
<div  class='comment'>已有评论：</div>
<div id="resText2" >
</div>


</body>
</html>


ajax不想全局 global:false 
