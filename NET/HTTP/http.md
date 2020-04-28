# HTTP知识汇总

## http报文格式

http报文可以分成两类：请求报文、响应报文

请求报文格式： 
> \<method> \<request-URL> \<version>  
> \<headers>  
> \<entity-body>

响应报文的格式：
> \<version> \<status>\<reason-phrase>  
> \<headers>  
> \<entity-body>

### 方法
|方法|是否包含主体|
|:-:|:-:|
|GET|否|
|HEAD|否|
|POST|是|
|PUT|是|
|TRACE|否|
|OPTIONS|否|
|DELETE|否|

### 状态码
|状态码|原因短语|含义|
|:-:|:-:|:-:|
|100|Continue|说明受到了请求的初始部分，请客户端继续。发起了这个状态码之后，服务器在收到请求之后必须进行响应。|
|101|Switching Protocols|说明服务器正在根据客户端的指定，将协议切换成update首部所列的协议|
|200|OK|请求没问题，实体的主题部分包含了所请求的资源|
|201|Created|用于创建服务器对象的请求（比如put）响应的实体中应该包含各种引用了已创建的资源的URL|
|202|Accepted|请求已被接受，但服务器还未对其执行任何动作。不能保证服务器会完成|
|203|Non-Authoritative Information|实体首部包含的信息不是来自于源端服务器，而是来自资源的一份副本|
|204|No Content||
|205|Reset Content||
|206|Partial Content||
||||
||||
||||
||||
||||
||||
||||
||||
