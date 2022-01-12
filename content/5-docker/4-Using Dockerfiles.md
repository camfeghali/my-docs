---
title: 'Using Dockerfile'
metaTitle: 'Using Dockerfile'
metaDescription: 'Using Dockerfile'
---

This page will include a sample Dockerfile and comments on the commands used in it.

```
#Define what base image to use
FROM httpd:2.4

#Allows you to run a standard bash command
RUN apt update -y && apt upgrade -y && apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists/

#Clean up file to add yours
RUN rm -f /usr/local/apache2/htdocs

#Specifiy which directory inside the container
WORKDIR /usr/local/apache2/htdocs

#Copy files from local machine to container.
#First argument is the location on the host relative to the Dockerfile where the information is copied from
#The second argument is the locationin in the container you want to copy the files to.
#Here we use . because we set the WORKDIR previously.
COPY ./web .
```

# Build

`docker build -t <image-name>:<tag> <path-to-Dockerfile>`
