# ZhiShi-v1.0
> 帮助开发者构建自己的知识体系，以左侧知识树，右侧展示对应的知识信息
> 整理自己的知识，便于查阅
> 1.0版本是基于html自己开发，不需要与数据库交互，使用起来比较简单。
</br>预览：https://yc-tao.github.io/ZhiShi-v1.0/
# 入门
	了解简单的html知识
# 部署
推荐部署到nginx，下面是nginx配置信息，提供参考
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
# 开始
> #### 部署成功后，进入docs，在data.json中
> ##### 1.可以编辑name、模板（用于显示属于自己模板）以及左侧知识树json信息，每一个知识节点要有name信息
> ##### 2.编辑每个节点对应的src，用于显示对应的知识信息，详情看demo。
# Issues
有问题可以添加issues，或者联系我
# 联系
1130147625@qq.com
