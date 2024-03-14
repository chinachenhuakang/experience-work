


# 微前端[qiankun]服务
    server {
        listen        9090;
        root          E:/nginx-1.22.0/html/test-bushu;
        server_name  localhost;

        # 后端接口代理
        location ^~ /gateway/ {
            if ($request_method !~ ^(GET|POST|OPTIONS)$ ) {
                return 403;
            }
            proxy_pass http://172.18.7.123:31101/;
            proxy_redirect    off;
            proxy_set_header        Host $host:$server_port;
            proxy_set_header        X-Real-IP $remote_addr;
            proxy_set_header        X-Forwarded-For $remote_addr; #$proxy_add_x_forwarded_for;
            proxy_set_header        X-Forwarded-Proto $scheme;
            # access_log /var/log/nginx/access-gateway.log;
        }


        # 主应用
        location / {
            try_files $uri $uri/ /index.html;
            # error_page 405 =200 @405;
            # error_page 405 =200  $request_uri;
            add_header 'Access-Control-Allow-Origin' '*';
        }
        # 子应用
        location /child/industry_admin {
            root   E:/nginx-1.22.0/html/test-bushu;
            index  index.html index.htm;
            try_files $uri $uri/ /child/industry_admin/index.html;
        }
    }


https://qiankun.umijs.org/zh/cookbook
