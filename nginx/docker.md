# nginx 
ps -ef | grep nginx
# docker mac nginx Server
`
docker run -d --name=nginx_webserver -p 80:80 -p 9080:9080 \
-v /Users/zenos/Downloads/Project/pc_front/dist:/usr/share/nginx/html/pc_dev \
-v /Users/zenos/Downloads/Other/Docker/nginx/conf.d:/etc/nginx/conf.d \
-v /Users/zenos/Downloads/Other/Docker/nginx/log:/var/log/nginx \
nginx

`
# docker window nginx Server
`
docker run -d --name=nginx_webserver -p 80:80 -p 9080:9080  -v E:/huatonghuhui/pc_front/dist:/usr/share/nginx/html/pc_dev  -v E:/Study/Docker/nginx/conf.d:/etc/nginx/conf.d  -v E:/Study/Docker/nginx/log:/var/log/nginx nginx

`
# 进入正在运行的容器
docker exec -it id /bin/bash  

# 查看容器基本信息
docker inspect mynginx