# lua

## 注释
```lua
-- xxx
--[[
xxxx
--]]
```

## 数据类型
* nil
* boolean
* number
* string
* function
* userdata (表示任意存储在变量中的C数据结构)
* thread (表示执行的独立线路，用于执行协同程序)
* table

```lua
print(type(10))  --number 
local b = 2   --局部变量，默认全局
x, y = y, x -- 类似js解构赋值
```

## while for repeat...until
```lua
while(condition)
do
  statements
end

for var=start,finish,step do  -- step default 1
  statements
end

repeat
  statements
until(condition)
```

## if
```lua
if(condition)
then
  statements
end

if(condition)
then
  statements
elseif(condition)
then
  statements
else
  statements
end
```

## function
```lua
optional_function_scope function function_name( argument1, argument2, argument3..., argumentn)
    function_body
    return result_params_comma_separated
end

function tset(...)
  for i = 1, select('#', ...) do
    local arg = select(i, ...)
    print("arg", arg)
  
test(1, 2, 3)
--[[
  arg  1
  arg  2
  arg  3
--]]
```

## 运算符
```lua
a..b -- 连接字符串
#'aaaa' -- 字符串长度
a ~= b
a^2
and
or
not
```

## string
```lua
string.upper(arg)
string.lower(arg)
string.gsub(main, find, replace, num)
string.sub(str, init [, finish])
string.find(str, substr[, init, [finish]])
string.reverse(str)
string.format(...) -- like c printf
string.char(int)
string.byte(str[, init])
string.len(str)
string.rep(string, n)
string.gmatch(str, pattern)
string.match(str, pattern)
```

## table 
```lua
arr = {'a', 'b'}
ipairs() -- 返回连续索引的内容，中断或者nil就停止
pairs() -- 键值对
-- 无状态迭代器
function square(iteratorMaxCount,currentNumber)
   if currentNumber<iteratorMaxCount
   then
      currentNumber = currentNumber+1
   return currentNumber, currentNumber*currentNumber
   end
end
for i, n in square, 3, 0 do 
  print(i, n) 

-- 多状态迭代器由闭包实现
function elementIterator (collection)
   local index = 0
   local count = #collection
   -- 闭包函数
   return function ()
      index = index + 1
      if index <= count
      then
         --  返回迭代器的当前元素
         return collection[index]
      end
   end
end

for element in elementIterator(array)
do
   print(element)
end

table.concat(table [, seq[, start[, finish]]])
table.insert(table, [pos,] value)
table.remove(table [, pos])
table.sort(table [, cmp])
```

## module

```lua
module = {}
module.constant = ''
return module
```

```lua
require("module")
require "module"
```

## 元表

```lua
mytable = setmetatable({}, {})
getmetatable(mytable) -- return mymetatable
__index
__newindex
__add
__sub
__mul
__div
__mod
__concat
__eq
__lt
__le
__call
__tostring
```

## 协同程序

```lua
coroutine.create()
coroutine.resume()
coroutine.yield()
coroutine.status()
coroutine.wrap()
coroutine.running()
```

## io

```lua
io.open(filename [, mode]) -- r w a r+ w+ a+ b +
io.input(filename)
io.output(filename)
io.write(str)
io.close()
io.read()
--[[
n  number
a  whole file
l skip endl, return fail on end of file
L keep endl, return fail on end of file
number read n bytes 
--]]
io.lines(filename)
```

## 错误处理

```lua
assert(a == 1, msg)
error(msg [, level]) -- 1 file and line number   2 which function throw the error  0  no position
if pcall(functionName[, args...]) then
-- no error
else
-- error
end
xpcall(f, msgh [, arg1, ...])
debug
```

## 垃圾回收
```lua
collectgarbage('collect')
collectgarbage('count')
collectgarbage('restart')
collectgarbage('setpause')
collectgarbage('setstepmul')
collectgarbage('step')
```


