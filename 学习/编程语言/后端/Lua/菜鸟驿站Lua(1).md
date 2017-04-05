特性:支持面向过程编程和函数式编程
自动内存管理;

windows 运行lua脚本 首先cd到脚本路径 然后lua.exe test.lua

多行注释
--[[
--]]


tab ={key="val1"}

tab1 = { key1 = "val1", key2 = "val2", "val3" }--只有值没有key则默认key为1
for k, v in pairs(tab1) do
    print(k .. " - " .. v)
end
 
tab1.key1 = nil -- 
for k, v in pairs(tab1) do
    print(k .. " - " .. v)
end


## boolean（布尔） ##
boolean 类型只有两个可选值：true（真） 和 false（假），Lua 把 false 和 nil 看作是"假"，其他的都为"真":


## string（字符串） ##
字符串由一对双引号或单引号来表示。
也可以用 2 个方括号 "[[]]" 来表示"一块"字符串。


在对一个数字字符串上进行算术操作时，Lua 会尝试将这个数字字符串转成一个数字:

字符串连接是..