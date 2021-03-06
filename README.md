# netty_proxy_server
基于Netty实现的代理服务器

功能：    http(s)和tcp数据的转发,实现了类似ngork的功能

大概流程：一共分为3个角色,我称它为 用户、服务端[server] 和 客户端[client]
```
用户 ----> 服务端 -----> 服务端下发指令 ------------> 客户端  ------------>
                                                                    访问对应的服务
用户 <---  服务端 <----  客户端返回数据给服务端 <----- 客户端  <-----------
```

使用方法：
```
    - 使用maven打包
    - 部署server的war包到服务器上,默认的用户名和密码是 admin/123
    - 运行client的jar包,java -jar client.jar 输入用户名和密码
    - 网页上打开server端,配置和端口后,运行即可,如果需要使用http代理,需要设置ie的代理服务
```

截图：
 ![image](https://github.com/GTale/netty_proxy_server/blob/master/screenshot/01.png)
 ![image](https://github.com/GTale/netty_proxy_server/blob/master/screenshot/02.png)
 ![image](https://github.com/GTale/netty_proxy_server/blob/master/screenshot/03.png)
