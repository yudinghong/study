# go study

## go 运行编译
```cmd
go run xxx.go
go build` xxx.go
```

## go 基础结构
```go
package main
import "fmt"
func main() {
    fmt.Println("Google" + "Runoob")
}
```

每个程序必须有一个`package main`, package 指明在哪个包。  
`func main()`必须有


声明变量
```go
var identifier type
var identifier = "xxx"

// 或者
a := "xx"
// 以下是错误示例
var a int 
a := 3
```

### 常量
```go
const a int = 3
const (
    a = 3,
    b = 4
)
```

### iota


### 运算符
& 取地址符号  
\* 指针符号

## 条件判断
```go
if a < 3{

}
else if a > 2{

}
switch mark {
    case 90: 
    case 80:  fallthrough // fallthrough 强制执行下一个case不管正确与否
    default: 
}

switch {
    case mark == 90: 
}


```
### select
```go
select {
    case communication clause  :
       statement(s);      
    case communication clause  :
       statement(s);
    /* 你可以定义任意数量的 case */
    default : /* 可选 */
       statement(s);
}
```

* 每个 case 都必须是一个通信
* 所有 channel 表达式都会被求值
* 所有被发送的表达式都会被求值
* 如果任意某个通信可以进行，它就执行，其他被忽略。
* 如果有多个 case 都可以运行，Select 会随机公平地选出一个执行。其他不会执行。否则：
    1. 如果有 default 子句，则执行该语句。
    2. 如果没有 default 子句，select 将阻塞，直到某个通信可以运行；Go 不会重新对 channel 或值进行求值。

```go
package main

import "fmt"

func main() {
   var c1, c2, c3 chan int
   var i1, i2 int
   select {
      case i1 = <-c1:
         fmt.Printf("received ", i1, " from c1\n")
      case c2 <- i2:
         fmt.Printf("sent ", i2, " to c2\n")
      case i3, ok := (<-c3):  // same as: i3, ok := <-c3
         if ok {
            fmt.Printf("received ", i3, " from c3\n")
         } else {
            fmt.Printf("c3 is closed\n")
         }
      default:
         fmt.Printf("no communication\n")
   }    
}
// no communication
```

## 循环
```go
for init; condition; post { }
for condition { }
//for 循环的 range 格式可以对 slice、map、数组、字符串等进行迭代循环。格式如下：
for key, value := range oldMap {
    newMap[key] = value
}
```

