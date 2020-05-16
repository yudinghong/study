# 基础学习

## 数据类型

js 定义了8种基本数据类型  
* Boolean
* Null
* Undefined 
* BigInt
* String
* Symbol
* Object
* Number

### BigInt
BigInt是为了解决Number精度问题的。js中数字都是以双精度64位存储。可以安全表示`-9007199254740991 (-(2^53-1))` 和`9007199254740991(2^53-1)`  
JS 提供`Number.MAX_SAFE_INTEGER`常量来表示 最大安全整数，`Number.MIN_SAFE_INTEGER`常量表示最小安全整数  
要创建BigInt，只需在整数的末尾追加n即可
```javascript
console.log(9007199254740995n);    // → 9007199254740995n
console.log(9007199254740995);     // → 9007199254740996
BigInt("9007199254740995");    // → 9007199254740995n
```

### Symbol
本质上是一种唯一标识符。

## ES6新增的对象

### Set WeakSet
```javascript
let set = new Set()
let set = new Set([1,2,3])
//方法有
/*
add()
clear()
delete()
entries() 返回一个迭代器对象
forEach(value, key, self) value === key
has()
values()

*/
```
WeakSet对象是一些对象值的集合, 并且其中的每个对象值都只能出现一次，WeakSet只能存对象类型的元素，比如：Object, Array, Function 等等；有了弱引用的WeakSet， 就不用担心内存泄漏了，如果别的对象不引用该对象， 这个对象会被垃圾回收机制自动回收；
weakSet可以用来保存DOM节点， 当节点被删除， weakSet里面的该节点如果不存在别的引用的话， 一段时间内会被内存回收

## Map WeakMap
```javascript
let map = new Map()
//方法有
/*
size()
delete()
entries()
forEach()
get(key)
has(key)
keys()
set(key, value)
values()
*/
```  
```javascript
let wm = new WeakMap()
/*
delete()
get(key)
has(key)
set(key, value)
*/
```

## iterable

## this
使用new对象的this指向创建的对象，不然就是普通函数执行

## 原型链

在对象实例和它的构造器之间建立一个链接（它是__proto__属性，是从构造函数的prototype属性派生的）

## 闭包

## 对象

### 对象的构造方式
```javascript

```
