# nginx 查询安装目录 


centos7怎么查看已经安装nginx
 我来答 分享 举报 浏览 13546 次
1个回答 #热议# 不考虑收入，你最想做什么工作？
一骑当后 
知道合伙人数码行家 推荐于2017-11-29
　　如果你nginx是rpm包安装的，直接用如下命令：
　　nginx -V　　
　　如果你是源码包编译安装，假如你的安装路径是/usr/local/nginx，那么你可以使用
　　/usr/local/nginx/sbin/nginx -V
　　注意是大写的V，这样你就可以看到nginx已经加载的模块了。

> /usr/local/nginx/sbin/nginx -V


# nginx 重启
进入nginx 目录
> ./nginx -s reload


# nginx 开启 gzip

    ##gzip https://www.cnblogs.com/mitang/p/4477220.html
	gzip on;
	gzip_min_length 1k;
	gzip_buffers 4 16k;
	#gzip_http_version 1.0;
	gzip_comp_level 2;
	gzip_types text/plain application/x-javascript text/css application/xml text/javascript application/javascript application/x-httpd-php image/jpeg image/gif image/png;
	gzip_vary off;
	gzip_disable "MSIE [1-6]\.";