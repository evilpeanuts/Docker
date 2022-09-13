# Docker

# nacos
`
 docker run --name nacos -d -p 8848:8848 --restart=always \
 -v /Users/zenos/Downloads/Other/Docker/nacos/logs:/home/nacos/logs \
 -v /Users/zenos/Downloads/Other/Docker/nacos/conf:/home/nacos/conf \
 nacos/nacos-server
`
# nacos run  restart
`
docker run --name nacos -d -p 8848:8848 --restart=always \
  nacos/nacos-server
`
# nacos Copy
`
  docker cp 805a64f686fa:/home/nacos/conf ./
`