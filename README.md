# ZhiShi-v1.0
### 构建自己的知识体系
	1、整理自己的知识，便于实时查阅
	1、以左侧知识树，右侧展示对应的知识信息
	3、所有数据自己配置，不需与数据库交互
	4、使用起来比较灵活、简单。
预览：https://yc-tao.github.io/ZhiShi-v1.0/
# 入门
	了解简单的html知识

# 部署

推荐部署到nginx 

#### 下载nginx
	http://nginx.org/en/download.html

下载nginx并解压，作者用的是nginx-1.14.2版本

#### 下载ZhiShi-v1.0，放入nginx的html目录，可参考

![githubusercontent](https://raw.githubusercontent.com/yc-tao/ZhiShi-v1.0/master/docs/images/nginx.png)  

#### 下面是nginx配置信息，提供参考
	
	server{

    		listen       8080;
	
    		server_name  localhost;
      
    		charset utf-8;
 
    		root html/ZhiShi/v1.0.1/build;
    		index index.html index.htm;
 
    		location / {
        		try_files $uri $uri/ /index.html;
    		}
		
    		location /dist/ {
			alias  html/ZhiShi/v1.0.1/build/;
    		}
		
    		error_page 500 502 503 504 /500.html;
    		client_max_body_size 20M;
    		keepalive_timeout 10;
	}

### 部署成功

访问 http://localhost:8080

![githubusercontent](https://raw.githubusercontent.com/yc-tao/ZhiShi-v1.0/master/docs/images/example.jpg)  

# 开始

### 部署成功后，进入docs，

#### 在data.json中
	1、编辑name，显示知识体系的标题以及尾部标题，以及版本信息
	2、编辑template，首页显示的内容
	3、编辑root，知识根节点
		<1>、name => 根节点名称
		<2>、display => 是否显示
	3、编辑data，数组对象形式，ztree的节点
		<1>、name => 知识名称（必填）
		<2>、src => 点击时，显示的页面地址
		<3>、children => 子信息节点
		<4>、iframe => 是否以iframe显示知识详情信息

#### 在docs下新建文件夹，创建html文件，可以参考demo.html
	1、编辑页面
		<1>、支持显示code，目前支持html、css、js
		<2>、支持显示基本的html内容
		<3>、支持显示图片
		<4>、支持在页面中使用jquery
	

# Issues

有问题可以添加issues，或者联系我

# 联系

1130147625@qq.com


