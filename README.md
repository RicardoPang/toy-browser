# toy-browser

a toy browser

### 目标：

可以向服务器端发 Request 请求，并解析服务器返回的 Response，将其中信息提取出来。

### 服务端程序

```javascript
const http = require('http');
const server = http.createServer((req, res) => {
  console.log('request receved');
  res.setHeader('Content-Type', 'text/html');
  res.setHeader('X-Foo', 'bar');
  res.writeHead(200, { 'Content-Type': 'text=plain' });
  res.end('ok');
});
server.listen(8088);
```

### 客户端（浏览器）程序

- Request
- 请求报文格式
  ![](https://cdn.nlark.com/yuque/0/2020/png/1251266/1589563753655-9a17d65d-66df-477e-995e-f5d7f51d5b59.png)

- Response
- 相应报文格式
  ![](https://cdn.nlark.com/yuque/0/2020/png/1251266/1589563779104-6f59f3f7-b2b7-4580-8f62-20c5f8b08ca4.png)

- 状态机
  ![](https://cdn.nlark.com/yuque/__puml/de3b7d5a9b9a00a6202ff9bfb0ef6927.svg)

1. clone the project, and go to src

```bash
cd toy-browser/src
```

2. install npm and node.js

3. install packages (css and images)

```bash
npm install
```

4. start the server

```bash
node server.js
```

5. open a new terminal, and start the client

```bash
node client.js
```
