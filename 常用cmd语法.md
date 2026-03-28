```
netstat -ano | findstr :808
taskkill /PID 12345 /F
```

```ZSH
Docroot is: /opt/homebrew/var/www

The default port has been set in /opt/homebrew/etc/nginx/nginx.conf to 8080 so that
nginx can run without sudo.

nginx will load all files in /opt/homebrew/etc/nginx/servers/.

To start nginx now and restart at login:
  brew services start nginx
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/nginx/bin/nginx -g daemon\ off\;
```

```zsh
MAC

worker_processes auto; # 自动匹配CPU核心数
events {
    worker_connections 1024;
    use kqueue; # Mac专属的事件模型
}

http {
    sendfile on; 
    tcp_nopush on; # 提升传输效率
    keepalive_timeout 65;
    
    # 日志格式优化
    log_format main '$remote_addr - $remote_user [$time_local] '
                   '"$request" $status $body_bytes_sent '
                   '"$http_referer" "$http_user_agent"';
}


先备份原有配置（防止改错）：
cp /opt/homebrew/etc/nginx/nginx.conf /opt/homebrew/etc/nginx/nginx.conf.bak
open /opt/homebrew/etc/nginx/nginx.conf
语法验证
nginx -t
重新启动
brew services restart nginx
或者：
nginx -s reload
端口监听
lsof -i :8080

# 确保目标目录存在
sudo mkdir -p /opt/homebrew/var/www/dist02

# 将构建输出复制到目标目录
cp -r dist/* /opt/homebrew/var/www/dist02/



```

```
常用CODE
⌘F2：一键选中当前单词的所有出现（无需先选中）
使用comd+shift+P 调出片段
使用
```

