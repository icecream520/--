Lua 已经占用的关键字 and,beadk,do else,elseif,end,false,for,function,if,in,local,nil,not,or,repeat,return,then,true,until,while

Lua多行要用[[
连接
]]
允许一行交换两个变量 ..用来连接stings或者数字
Lua标准输出io.write("Hello from Lua")
io.write("Hello from Lua") 就算换新行还是在使用了空的print

## Tables ##
a={1,2,3} -- {} //创建一个空的table
table不是直接打印出来

table = {}; // 创建一个空的table
table.Street = "30s" 
print(table.Street);// 字典


## if语句 ##
if a==1 then
   print("")
end

if then

eles

end
//总结就是if else else if else
只要不是最后一个条件都要加上 then 最后条件则要加上end

a=1
b=(a==1) and "one" or "not one"
====
 a = 1
if a==1 then
 b="one"
else
b="not one"
end


### while语句 ###
a=1
while a~=5 do --~=代表着不等于
  a=a+1
  io.write(a.."")
end

## repeat until 循环 ##
a=0
repeat
 a=a+1
 print(a)
until a==5

#### for语句 ####
for var=ex1,exp2,exp3 do something end
=c# for(int i=exp1;i<=exp2;i+=exp3)
{
something;
}

-- for语句的Generic for变体
-- Sequential iteration form.
 
for key,value in pairs({1,2,3,4}) do print(key, value) end
## -- Example 24   -- Printing tables. ##
-- 用简单的方式遍历table结构，并输出
-- Simple way to print tables.
 
a={1,2,3,4,"five","elephant", "mouse"}
 
for i,v in pairs(a) do print(i,v) end
 
 
-------- Output ------
 
1       1
2       2
3       3
4       4
5       five
6       elephant
7       mouse
 

for i,v in pairs(a) do print(i,v)end

遍历 a 新建两个变量i,v i是排序数 v是值

-- break is used to exit a loop. 
-- break关键字用于跳出循环，当然return也可以，不过有区别
 
a=0
while true do
    a=a+1
    if a==10 then
        break
    end
end
 
print(a)

Lua (Command Line) 这里清屏的方式是：

os.execute("cls")

就是执行了DOS中的清屏命令！