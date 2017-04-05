Lua (Command Line) 这里清屏的方式是：

os.execute("cls")

就是执行了DOS中的清屏命令！

带返回值的函数调用 Lua里面对函数带不带参不敏感,你可以多带几个反正只看名字


函数如果带参数 你传参进去如果参数不对多了舍弃,少了则赋值为nil。


--在Lua中,默认声明变量为全局变量,以local为修饰符的为局部变量,局部变量只在所属语句的块内生效

--Lua中的库有math,string,table,input/output & operating system facilities

--Lua扩展类库
