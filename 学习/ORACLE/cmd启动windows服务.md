    sc create NG.PatchCenter.Service binpath= "E:\Php下载\MyFirstWindowsService\MyFirstWindowsService\bin\Debug\MyFirstWindowsService.exe -service" displayname= "NG.PatchCenter.Service" depend= Tcpip start= auto 
//windows服务cmd启动
    sc delete NG.PatchCenter.Service
//windows服务cmd删除
1.public Timer(TimerCallback callback, object state, int dueTime, int period);
2.public Timer(TimerCallback callback, object state, long dueTime, long period);
3.public Timer(TimerCallback callback, object state, TimeSpan dueTime, TimeSpan period);
4.public Timer(TimerCallback callback, object state, uint dueTime, uint period);

a、callback：望文生意，肯定表示一个回调，它是标识希望由一个线程池线程回调的方法。当然它的类型必须和System.Threading.TimerCallback委托类型匹配，如下所示：

1
public delegate void TimerCallback(object state);
b、state：每次调用回调方法，向回调方法传递的状态数据，如没有，可以为null；

c、dueTime：在首次调用回调方法之前要等待多少毫秒。如希望立刻调用回调方法，该参数指定为0即可。

d、period：指定了以后每次调用回调方法之前要等待多少毫秒（理解成下一次和本次调用的时间间隔即可）。如果为该参数传递Timeout.Infinite(或者直接写-1)，线程池线程只调用回调方法一次（那也就没有必要用计时器了）。