## PaN e-Learning pages

This is a help for potential content creators on [pan-learning](https://pan-learning.org).


### Creating your own docker container 

If you need your own JupyterHub environment with software not currently included in any of the current containers you need to build your own docker container. Information regarding docker can be found at [https://docs.docker.com/](https://docs.docker.com/). 

If you do not have any prior experience, this is not a problem. 
Download and install docker following the instructions on [their website](https://docs.docker.com/get-docker/). 

#### Practise building a container. 

```markdown
docker pull moving-northwards/crispy 

docker run -p 8888:8888 moving-northwards/crispy 
```


