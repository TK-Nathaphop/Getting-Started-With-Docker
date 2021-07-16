# Docker Basic

## What is different between image and container?

|   Build time   |       Run time       |
| :------------: | :------------------: |
| Template of VM | Virtual Machine (VM) |
|     Image      |      Container       |

## Build an image

```
docker image build -t username/repo:version .
```

## See image list

```
docker image ls
```

## Push image to docker hub

```
docker image push dockerUsername/repository:version
```

## Delete image

```
docker image rm dockerUsername/repository:version
```

## Run Docker image to container

```
docker container run -d --name app-name -p 8000:8000\
dockerUsername/repo:version
```

**Note**: 8000 → Port expose : 8080 → Port from app in container
**Note 2**: Docker will first look for a local copy image. But if it don’t found, it will pull from docker hub.

## Stop Docker container

```
docker container stop app-name
```

## Start Docker container

```
docker container start app-name
```

## Remove Docker container

```
docker container rm app-name
```

## Ctrl+P+Q used to leave from Container

Used Ctrl+P+Q to leave container. Because, if we used command `exit` to exit from container without anything run inside, container will stop. So, it is better to leave a container with Ctrl+P+Q.
