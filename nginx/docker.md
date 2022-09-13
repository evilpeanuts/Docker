# nginx 
ps -ef | grep nginx
# docker mac nginx 2b_h5 pc_dev insuranceh5 Server
`
docker run -d --name=nginx_webserver -p 80:80 -p 6666:6666 -p 7777:7777 -p 8888:8888  -p 9999:9999  \
-v /Users/zenos/Downloads/Project/bigFamily/h5/dist/build/h5:/usr/share/nginx/html/2b_h5 \
-v /Users/zenos/Downloads/Project/bbw/b2b_pc/dist:/usr/share/nginx/html/pc_dev \
-v /Users/zenos/Downloads/Project/健康险/insuranceH5/dist:/usr/share/nginx/html/insuranceh5 \
-v /Users/zenos/Downloads/Other/Docker/nginx/conf.d:/etc/nginx/conf.d \
-v /Users/zenos/Downloads/Other/Docker/nginx/log:/var/log/nginx \
nginx
`
# docker mac nginx portal reporting 2b_h5 pc_dev insuranceh5 Server
`
docker run -d --name=nginx_webserver -p 80:80 -p 6666:6666 -p 7777:7777 -p 8888:8888  -p 9999:9999 -p 9801:9801 -p 9810:9810 \
-v /Users/zenos/Downloads/Project/microFrontEnd/PortalApp/dist/:/usr/share/nginx/html/portal \
-v /Users/zenos/Downloads/Project/microFrontEnd/px-app-report/dist/:/usr/share/nginx/html/reporting \
-v /Users/zenos/Downloads/Project/bigFamily/h5/dist/build/h5:/usr/share/nginx/html/2b_h5 \
-v /Users/zenos/Downloads/Project/bbw/b2b_pc/dist:/usr/share/nginx/html/pc_dev \
-v /Users/zenos/Downloads/Project/健康险/insuranceH5/dist:/usr/share/nginx/html/insuranceh5 \
-v /Users/zenos/Downloads/Other/Docker/nginx/conf.d:/etc/nginx/conf.d \
-v /Users/zenos/Downloads/Other/Docker/nginx/log:/var/log/nginx \
nginx

`
# docker window nginx Server
`
docker run -d --name=nginx_webserver -p 80:80 -p 9080:9080  -v E:/huatonghuhui/pc_front/dist:/usr/share/nginx/html/pc_dev  -v E:/Study/Docker/nginx/conf.d:/etc/nginx/conf.d  -v E:/Study/Docker/nginx/log:/var/log/nginx nginx


# redis
docker run -itd --name redis -p 6379:6379 -appendonly yes \
-v /Users/zenos/Downloads/Other/Docker/redis/conf/redis.conf:/etc/redis/redis.conf \
-v /Users/zenos/Downloads/Other/Docker/redis/data:/data \
redis

`


# docker window mysql 8 Server
`
docker run -itd --name mysql8019 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 mysql:8.0.19

#--mount type=bind,source=E:/Study/Mysql/8/conf/my.cnf,target=/etc/mysql/my.cnf
#--mount type=bind,source=E:/Study/Mysql/8/conf/conf.d,target=/etc/mysql/conf.d 
#--mount type=bind,source=E:/Study/Mysql/8/data,target=/var/lib/mysql

`

# docker window mysql 5.7.27 Server
`
docker run -itd --name mysql5727 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=123456 -v E:/Study/Mysql/5.7.27/conf/:/etc/mysql/ -v E:/Study/Mysql/5.7.27/data:/var/lib/mysql  -v E:/Study/Mysql/5.7.27/logs:/var/log/mysql mysql:5.7.27
`

# docker window mysqls connect 5.7.27 Server
`
docker run -it --network host --rm mysql:5.7.27 mysql -h 127.0.0.1 -p3306 --default-character-set=utf8mb4 -uroot -p
`

#

# docker window redis 5.7.27 Server
`
docker run -itd --name redis507 -p 6379:6379 redis:5.0.7

#


# docker window redis 5.7.27 Server
`
docker run -it --network host --rm redis:5.0.7 redis-cli

#

`
# 进入正在运行的容器
docker exec -it id /bin/bash  

# 查看容器基本信息
docker inspect mynginx

# 复制  宿主机 到 容器
`
docker cp /www/runoob 96f7f14e99ab:/www/

` 