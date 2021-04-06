# node-server
node服务

- 启静态服务
  ```js
  ./server/index.js
  ```

- nginx配置静态服务
```bash
server {
  ...
  location / {
    try_files $uri /index.html
  }
}
```