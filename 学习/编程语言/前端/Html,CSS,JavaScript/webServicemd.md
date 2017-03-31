# Web Service #
是一种可以接收从Internet或者Intranet上的其它系统中传递过来的请求.通过SOAP在Web上提供的软件服务，使用WSDL文件进行说明，并通过UDDI进行注册。
PushMsgService
首先拿到数据了，但是一个string，这时候我们要把这个数据分成两部分放入database里面，先判断这个tab里面有没有数据，如果没有则insert，如果有则跳过

protected void Button1_Click(object sender, EventArgs e)
   {
       localhost.Service aa = new localhost.Service();
       Label1.Text =Convert.ToString( aa.GetSum(Convert.ToInt32(TextBox1.Text.Trim()), Convert.ToInt32(TextBox2.Text.Trim())));
   }