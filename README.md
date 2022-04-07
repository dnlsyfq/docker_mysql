
### Command
* check docker images
```
docker images
docker rmi <container> -f
docker logs <name> -f
docker exec -it <name> bash
curl http://localhost:9200
curl -X PUT http://localhost:9200/newindex
curl -X GET http://localhost:9200/newindex
curl -X GET http://localhost:9200/newindex?pretty

```

* check docker container running , all
```
docker ps
docker ps -a
docker rm <container>
```

* stop docker container
```
docker stop <container ID >
```
# MySQL

### Method 1 
1. Find images at docker hub
2. Run images , create container
```
docker run -d --name <name> -p 3306:3306 -e MYSQL_ROOT_PASSWORD=<password> mysql:latest

// localhost port already is being in used. Change to another port.
docker run -d --name <name> -p 3366:3306 -e MYSQL_ROOT_PASSWORD=<password> mysql:latest
```
3. SSH to container
```
docker exec -it <name> bash
```

---

# Maria DB

* run images , create container
```
docker run -d --name <name> -e ALLOW_EMPTY_PASSWORD=yes -e MARIADB_USER=<name> -e MARIADB_DATABASE=<db name> -e MARIADB_PASSWORD=<password> docker.io/bitnami/mariadb:10.1-debian-10
```

---

# Laravel

* images
```
```

* linux command
```
ip addr

```

# Elastic Search



* pull images
```
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.12.1
```

* run images , create container
```
docker run -d --name elasticsearch -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.12.1
```