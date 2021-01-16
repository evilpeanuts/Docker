# mongodb 

# mongodb mac nginx Server
`
docker run -itd --name mongo -p 27017:27017 mongo:4.2.6

`
# mongodb mac nginx Server
`
docker run -d --name=mongo -p 27017:27017 \
-v /Users/zenos/Downloads/Other/Docker/mongodb/var/lib/mongodb:/var/lib/mongodb \
-v /Users/zenos/Downloads/Other/Docker/mongodb/var/log/mongodb:/var/log/mongodb \
mongo:4.2.6

`