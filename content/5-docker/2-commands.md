---
title: 'Commands'
metaTitle: 'List of docker commands, their use and flags'
metaDescription: 'List of docker commands, their use and flags'
---

# Pull image

```
docker pull <image-name>:version
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
- `-v` Used to mount a volume from local inside the container
- `ro` Used to define Read Only permissions for the container

# Stop container

```
docker stop <image-name>
```

# Remove container

```
docker rm <container-name>
```
