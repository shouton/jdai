# Mongodb

## the steps
1. ubutun
2. docker
```
sudo snap install docker 
```
3. docker install MongoDB image
``` 
sudo docker pull mongo:latest
```
4. create docker-compose.yml in /HOME
```
```
5. start docker container
```
docker-compose up -d
```
6. go into mongodb
```
docker-compose exec mongo bash
mongo admin -u cbre -p
```
Note: you can do it in docker, but i suggest you do it from GUI client
```mongoshell
show databases
use deal
-- show tables
show collections
db.hoge.insert({ name: "test" })
db.hoge.find()
...
exit
```
7. access from python

8. the sample code
main.py
```python
from pymongo import MongoClient
# use docker image name instead of the hostname 
client = MongoClient('mongo', 27017)
```

9. stop the container
```bash
docker-compose down
```

the reference
https://qiita.com/mistolteen/items/ce38db7981cc2fe7821a

10. install mongodbsqld

https://docs.mongodb.com/bi-connector/master/tutorial/install-bi-connector-debian/
```
mongosqld install --config /root/mongodb-bi-linux-x86_64-ubuntu1804-v2.13.4/example-mongosqld-config.yml 
mongosql service installed
root@ip-10-0-0-6:~/mongodb-bi-linux-x86_64-ubuntu1804-v2.13.4# 
systemctl start mongosql.service
systemctl enable mongosql.service
tail -f /var/log/mongosqld.log

```

11. setup ssl for mongodbsdqld

https://docs.mongodb.com/bi-connector/current/tutorial/ssl-setup/

#### done!
