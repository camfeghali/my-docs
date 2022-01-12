---
title: 'Commands'
metaTitle: 'List of docker commands, their use and flags'
metaDescription: 'List of docker commands, their use and flags'
---

# Pull image

```
docker pull <image-name>:version
```

# List images

```
docker images
```

# List running processes (container)

```
docker ps
```

### To list all containers, running or stopped

```
docker ps -a
```

# Run container

```
docker run --name <container-name> -p <server-port>:<container-port> -v <local-dir-absolute-path>:<container-dir-absolute-path>:ro -d <image-name>
```

- `-d` Used to run in detached mode (in the background)
- `-v` Used to mount a volume from local inside the container.
- `ro` Give Read Only permissions to the container on the volume.
- `--rm` Used to remove a container when stopped. Will also removed anonymous volume created for it.

# Stop container

```
docker stop <image-name>
```

# Remove container

```
docker rm <container-name>
```

# List Volumes

```
docker volume ls
```

# Create volumes

```
docker volume create <volume-name>
```

# Delete unused volumes

Will only delete volumes used by non-existant containers

```
docker volume prune
```

# Inspect

## Inspect mounted volume

```
docker inspect <container-name> -f '{{ json .Mounts }}' | python -m json.tool
```

# List Networks

```
docker network ls
```

# Create Networks

```
docker network create <network-name>
```

# To run a container on a specific network

```
docker run -d --name <container-name> --network <network-name> <image-name>
```
