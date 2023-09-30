# OpenLayer-GIS Test
This is testing for layer create with OpenLayer

# With docker-compose method - easy way

#### Build
```
docker-compose up -d
```

### Rebuild - If any change in docker file
```
docker-compose up -d --build
```


# Trying to Ready Environment
## Docker method only for container based development
Need to enter the contaner shell and then work under the container, best practice because, if change any localfolder under container shell not sync and if change under container shell the local dir not sync or notify.
It's just for checking or practice purpose. Otherwise use the docker-compose method.

### node install with docker
docker build -t <docker image name> <path>
```
docker build -t openlayer .
```

### Enter to inner of image

Check Images
```
docker images
```

Result
```
asifulmamun-office@AMD-R7:/var/www/openLayer-map-api$ docker images
REPOSITORY              TAG       IMAGE ID       CREATED          SIZE
openlayer               latest    14af6dca4abc   32 seconds ago   182MB
```

Docker Image Run RUN
docker run <imagName>
```
docker run openlayer
```


#### Run container with sh/bash
docker run -it --name <containerName> <imgName> sh
```
docker run -it --name openlayercontainer openlayer sh
```

#### Start/Run again exist container
docker start <containerName/ID>
```
docker start openlayercontainer
```

Run
docker exec -it <containerName/ID> sh
```
docker exec -it openlayercontainer sh
```

Stop
```
docker stop openlayercontainer
```

Run with port - skipped result, if don't want to skip result try without `-d` flag
docker run -d -p 3000:3000 --name <containerName> <imgName>
```
docker run -d -p 3000:3000 --name openlayercontainer openlayer
```

See all containers
```
docker ps -a
```

Log check of container
docker logs <containerName>
```
docker logs openlayercontainer
```

Delete container
docker rm <containerName>
```
docker rm openlayercontainer
```

Forces
docker rmi -f <containerName>
```
docker rmi -f openlayercontainer
```

Delete Image
docker rmi <imgName>
```
docker rmi openlayer
```

Forces
docker rmi -f <imgName>
```
docker rmi -f openlayer
```

Logs
docker logs <imgID/Imagename>
```
docker logs c53d45ca8a5e
```