# Docker

**List running containers :**
```
docker ps
```

**List all containers:**
```
docker ps -a
```

**Stop a container:**
```
docker kill d4
```

**Remove a container:**
```
docker rm d4
```

**List images:**
```
docker images
```

**Delete image:**
```
docker rmi d4
```

**List port forwarded for an image:**
```
docker port d4
```

**Run a container:**
```
docker run -it <image name> <command>
```

**MySQL for dev in a container:**
```
docker run -d --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root -v PATH:/var/lib/mysql mysql
```

**Mongo for dev in a container:**
```
docker run -d -p 27017:27017 --name mongodb mongo -v PATH:/data/db
```
