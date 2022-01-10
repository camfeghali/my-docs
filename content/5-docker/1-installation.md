---
title: 'Installation & Initialization'
metaTitle: 'Installing Docker'
metaDescription: 'Installing Docker'
---

The following is for a CentOS distribution, steps may vary for another linux distro.

# Installation

Run the following to install docker dependencies.

```
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

Run the following to get the latest docker version's repo.

```
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo/
```

Install docker

```
sudo yum -y install docker-ce
```

# Enable Docker daemon

Using systemd

```
sudo systemctl enable --now docker
```

# Enable user Permissions

We will allow our user to use docker without sudo permissions by adding our user to the `docker` group.

```
sudo usermod -aG docker <username>
```

To see our user in the `docker` group, we must log back in and run `groups`

We can now run `docker ps` to see running docker containers.
