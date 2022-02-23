---
permalink: /docs/docker/
classes: wide
title: Try out docker
---


If you need a JupyterHub environment with applications/modules not included in any of our current docker images, you can custom build your own. Complete documentation for docker can be found at [https://docs.docker.com/](https://docs.docker.com/). 


## Creating your own docker image

If you are new to docker, this is not a problem. Here we will guide you through. 

1. Download and install docker following the instructions on [docker's website](https://docs.docker.com/get-docker/).  
Be aware that Mac and Windows users will install 'docker desktop' but Linux users currently interact with docker purely through a terminal.  
<br>
2. Practice pulling one of our images from [Docker Hub](https://hub.docker.com/).
```
docker pull movingnorthwards/crispy 
```
(Linux users: If you wish to avoid typing `sudo` with each docker command you can become root with `sudo -i`.)
The movingnorthwards/crispy:latest version is automatically pulled. In other cases you might specify a version by explicitly giving the tag: `example/image:1.0.0`.

3. Try running the image as a container on your own computer. This will help you understand how the containers work on our e-learning platform. 
```
docker run -d -p 8888:8888 --name test moving-northwards/crispy 
```
Check out the container logs. 
```
docker logs test
```
At the bottom of the output you will see a similar message to: 
```  
    To access the notebook, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/nbserver-7-open.html
    Or copy and paste one of these URLs:
        http://29d5bca97b1d:8888/?token=8a93c688b03a17b597035daaf9d6b134e1465b04afafd717
     or http://127.0.0.1:8888/?token=8a93c688b03a17b597035daaf9d6b134e1465b04afafd717
```
Open the URL in your browser. You can then upload your Jupyter notebook to test if it runs. You can also test with our [notebook that uses Crispy](https://github.com/mretegan/crispy-pan-learning). 

4. To try building your own container you can copy our [simplest dockerfile](https://github.com/moving-northwards/docker4pan-learning/blob/main/Crispy/Dockerfile) and edit to add your own python modules or applications. Use `RUN` before a git/pip/bash command. 

{% include note.html content="Each RUN command creates a new layer. Avoid this by combining commands into one RUN command. Read about best practices [here](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)" %}


## 10 essential docker commands

For a full list see [https://docs.docker.com/engine/reference/commandline/docker/](https://docs.docker.com/engine/reference/commandline/docker/) and note that `--help` will show all the options for each command. 

##### 1. Pull an image from Docker Hub
```
docker pull docker/image:example
```
##### 2. Build your image from your dockerfile
```
docker build -t image_name:tag path/to/dockerfile
```
We recommend you set your tag to 'latest'. If you have a Docker Hub account you would call your image `dockerhub_name/image_name:tag`.
##### 3. Run an image
```
docker run -d -p 8888:8888 --name container_name  image_name:tag
```
The `-d` option detaches the container so it runs in the background of your terminal. The container_name can be anything you choose and is simply used to identify the container instance on your computer. If you do not add it, one will randomly be assigned (my favorites have been amazing_tesla and wizardly_feynman). The `-p` tag is for setting the port to 8888:8888.
##### 4. See which containers are running (process status)
```
docker ps 
```
Add `-a` to see _all_ containers (running and exited).
##### 5. Stop a container
```
docker stop container_name
```
##### 6. Restart an exited container
```
docker start container_name
```
##### 7. Check the logs of a container
```
docker logs container_name
```
##### 8. Check the logs of a container
```
docker logs container_name
```
##### 9. Check the logs of a container
```
docker logs container_name
```
##### 10. Delete a container
```
docker rm container_name
```
Use `docker image rm image_name` to delete an image. 

{% include note.html content="`--help` can be used with every docker command to show you the full list of options." %}

## Pushing to Docker Hub

Once built, you can of course push your image to Docker Hub. However, if you put your dockerfile on GitHub, we can also do this for you. The advantage here is that we can then rebuild it regularly if elements have updated. For example if the base notebook from docker stacks or nbgitpuller. 

#### More to be added to this section! 