# Docker Swarm

Docker Swarm is a cluster of manager nodes and worker nodesl.

Manager hosts the control panel feature with worker. It is recommended odd number for managers to known which group of managers have higher majority when there are network segmentation/failure.

If there are any failure in some node, the docker swarm will automatically manage.

## Initial manager

```
docker swarm init --advertise-addr=ip-of-your-manager-node
```

## Get manager token to add manager

```
docker swarm join-token manager
```

Then copy the command that appear and run to manager node

## Get worker token to add worker

```
docker swarm join-token worker
```

Then copy the command that appear and run to worker node

## See node distribution

```
docker node ls
```

## Create service to run on Docker swamp

```
docker service create --name app-name -p 8080:8080\
--replicas 3 image-name
```

Create app to run with 3 replicas.

## See service list

```
docker service ls
docker service ps app-name
```

Used to see docker container

## Scale up the service

Easily to scale up the service that currently running

```
docker service scale app-name=10
```

## Deploy Docker stack

Using docker-compose to deploy into Docker swamp

```
docker stack deploy -c docker-compose.yml app-name
```

## See Docker stack container

```
docker stack ps app-name
```

## Remove Docker stack

```
docker stack rm app-name
```
