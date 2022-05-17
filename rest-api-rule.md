# RESTful API

1. REST是一种架构风格，面向资源进行操作，用 URI来标记资源
2. REST统一了接口、统一了URI；支持无状态；可缓存；支持分层；支持按需代码

## 具体方法：
1. 统一接口，统一URI

原来可能我们是这样定义接口的：
> http://xxx.com/api/v1/getUserInfo
>
> http://xxx.com/api/v1/addUserInfo
>
> http://xxx.com/api/v1/updateUserInfo
>
> http://xxx.com/api/v1/deleteUserInfo     

REST规范定义接口：
> http://xxx.com/api/v1/user, GET, 获取用户信息
>
> http://xxx.com/api/v1/user, POST, 新增用户信息
>
> http://xxx.com/api/v1/user, PUT,  修改用户信息
>
> http://xxx.com/api/v1/user, DELETE, 删除用户信息

![rest-api](https://markdownpicsupload.oss-cn-beijing.aliyuncs.com/img/rest-api.png)

2. 不需要有状态才能操作

REST约束：客户端和服务器在通信上是无状态的。       

无状态是指客户端到服务器的每一个请求都包含了这次请求所需要的信息。    

举个栗子：比如月底发工资了，你需要查询这个月薪资的薪资明细。需要先登录，登录后才能进行查询。登录就是一种状态，没有登录系统就查不了，因此它是有状态的，有依赖条件的。        

如果是REST方式，只要你传给服务器说明需要查询哪个用户的信息，服务器在**验证你的身份**后，把薪资5000，扣了社保100，公积金200这些详细信息返回给你。

3. 可缓存请求

服务器可以标记响应的内容是否可以被客户端缓存。如果是可缓存的，那么客户端可以在之后相同的请求重复使用这个数据。

4. 支持分层系统

服务器和客户端之间允许有多个不同的中间组件，比如代理层，网关层，缓存组件。

5. 支持按需代码（可选）


