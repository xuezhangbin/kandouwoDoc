#客户端与服务器交互规则

##1 客户端首次连接服务器
* 构造register token，发送服务器
* 服务器处理token，返回access token

##2 客户端请求获取access token
* 客户端构造login token，发送服务器
* 服务器处理token，返回access token

##3 客户端请求敏感数据操作
* 客户端构造login token，发送服务器
* 服务器验证token，响应请求
* 不返回access token

##4 客户端请求次敏感数据操作
* 客户端发送access token给服务器
* 服务器验证token，接受或拒绝客户端请求并响应
* 返回是否需要客户端重新获取access token

##5 客户端请求非敏感数据操作
* 客户端发送请求给服务器
* 服务器接受请求并响应
* 返回相关数据
