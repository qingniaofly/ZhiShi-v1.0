# ZhiShi-v1.0
帮助开发者构建自己的知识体系，
你需要知道html的相关知识，
支持html、css、js、图片等方式
</br>预览：https://yc-tao.github.io/ZhiShi-v1.0/
# 部署
将此包下载下来，然后部署到nginx</br>


	server{

    listen       8080;
	
    server_name  localhost;
      
    charset utf-8;
 
    root html/ZhiShi/build;
    index index.html index.htm;
 
    location / {
        try_files $uri $uri/ /index.html;
    }
		
    location /dist/ {
	alias  html/ZhiShi/build/;
    }
		
    error_page 500 502 503 504 /500.html;
    client_max_body_size 20M;
    keepalive_timeout 10;
}
# Issues
有问题可以添加issues，或者联系我
# 联系
1130147625@qq.com
