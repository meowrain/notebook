# node.js

## http模块

### 01.创建服务器

```javascript
let http = require("http");
//创建服务器
http.createServer((req, res)=>{
    //接收浏览器传的参数 返回渲染的内容
}).listen(3000,()=>{
    console.log("server start")
})
```

node服务器的简单使用

```javascript
let http = require("http");
//创建服务器
http.createServer((req, res) => {
    //接收浏览器传的参数 返回渲染的内容
    //req 接受浏览器传的参数
    //res 返回渲染的内容
    res.writeHead(200, {"Content-Type": "text/html;charset=utf-8"})
    //给浏览器一个响应头
    res.write(`
    <b>你好，服务器已启动</b>
    `)//响应报文
    res.end();
}).listen(3000, () => {
    console.log("server start")
})
```



### 02.进阶使用

req.url //获取访问路径

```javascript
let http = require("http");
//创建服务器
http.createServer((req, res) => {
    //接收浏览器传的参数 返回渲染的内容
    //req 接受浏览器传的参数
    //res 返回渲染的内容
    console.log(req.url); //获取请求路径
    res.writeHead(200, {"Content-Type": "text/html;charset=utf-8"})
    //给浏览器一个响应头
    res.write(`
    <b>你好，服务器已启动</b>
    `)//响应报文
    res.end();
}).listen(3000, () => {
    console.log("server start")
})
```

