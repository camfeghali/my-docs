---
title: 'Container Networking'
metaTitle: 'Container Networking'
metaDescription: 'Container Networking'
---

By default, Docker creates 3 networks, a **bridge**, **host** and **null** networks.

#### Bridge networks

Networks that provide networking for containers that make an application. You can create custom one.
Containers from the same bridge network can ping each other by name.

#### Host network

Refers to the machine's network and makes everthing the machine can access accessible by the container.

You can list networks with `docker network ls`

To view which network a container is running on, we can use `docker inspect <container-name>`, and look at the bottom for "Networks".

### To create a custom bridge network.

```
docker network create <network-name>
```

### To run a container on a specific network

```
docker run -d --name <container-name> --network <network-name> <image-name>
```

### To run a container on localhost's network, use `host`

```
docker run -d --name <container-name> --network host <image-name>
```
