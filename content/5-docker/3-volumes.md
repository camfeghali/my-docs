---
title: 'Working with volumes'
metaTitle: 'Working with volumes'
metaDescription: 'Working with volumes'
---

Volumes are used to store container data.
Volumes are great for storing **configuration files, static shared files, or any stateful information you need in your containers**

# Goals

1 - Discover anonymous volumes.
2 - Create volumes.
3 - Use the volume in containers.
4 - Clean up unused volumes.
5 - Back up & Restore volumes.

## 1 - Discover anonymous volumes.

You can list volumes by running `docker volume ls`

An example container that creates volumes on start is `postgres` images. That's because a postgres container doesn't want to lose its data if it shuts down.

These volumes are called anonymous volumes because they are created with a name that is comprised of random hex characters.

To see an example, you can run `docker run --name db1 -d postgres:12.1`, followed by `docker volume ls`. You will see a volume that was created by the postgres container.

Running a container with the `--rm` flag will remove the container AND the anonymous volume created with it when stopped.

## 2 - Creating and using a Volume.

### Create the volume

You can create a volume with `docker volume create <volume-name>`.
You can see it in the list by running `docker volume ls`.

Volumes live in a protected space, so we need to use `sudo` to add data to it.

To copy a file or dir to a volume:

```
sudo cp -r <origin-dir-absolute-path> /var/lib/docker/volumes/<volume-name>/_data
```

## 3 - Use the volume

```
docker run -d  --name <container-name> -p 80:80 -v <volume-name>:<container-dir-absolute-path>:ro httpd:2.4
```

## 4 - Clean up unused volumes.

Will only delete volumes used by non-existant containers

```
docker volume prune
```

## 5 - Back up & Restore volumes.

Docker volume data is stored in protected space. So we need to be root.

`sudo su -`

To find where on the machine the volume data is stored, we use:

```
docker volume inspect <volume-name>
```

The location is found in the `Mountpoint` key.

We us the tar linux utility to create a zipfile.

```
tar czf /tmp/website_$(date +%Y-%m-%d-%H-M).tgz -C <volume-data-path> .
```

To extract a backup:

```
tar xf <backup-path> <backup-destination>
```
