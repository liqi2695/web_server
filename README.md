[此项目已经移到新库webServer](https://github.com/liqi2695/webServer/tree/master)
# 介绍
* web服务器-采用c++11网络编程编写的可支持PHP脚本的web服务器

# 环境
* OS: Ubuntu 18.04.2
* Complier: g++ 7.4.0

# 技术栈
* 采用c++11的多线程库，支持多个客户端连接。
* 考虑到服务器的性能问题，引入内存池，能很好的防止产生内存碎片，引起内存泄漏等问题。考虑到多线程，加入线程锁，防止死锁。
* 支持http的get请求，调用php-cgi可解析php页面文件
* 使用正则表达式获取请求页面文件
* 重新封装Tcp/IP中的bind、accept、connect等函数，考虑到代码的复用问题，将其编译成动态链接库.so文件。能够提高代码编译的速度，以及使代码更加简洁
* 用面向对象思想封装各个类，提高代码的易读性，可复用性


# Run
* 在xscoket中输入指令make，编译动态链接库
* 然后在tcpserver中输入指令make，运行服务器
* 服务器开启，在浏览器中输入  本机IP:端口号/index.html   

