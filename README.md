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

- apache配置静态服务
```bash
RewriteBase /
RewriteRule ^index\.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /index.html [L]
```