<img src="/assets/img/PaNelearning.png"
     alt="PaN e-Learning logo"
     style="width: 300px" />
     
     
This page is an additional for potential content creators on [PaN e-Learning platform](https://pan-learning.org).


## Creating your own docker container 

If you need your own JupyterHub environment with software not currently included in any of the current containers you need to build your own docker container. Information regarding docker can be found at [https://docs.docker.com/](https://docs.docker.com/). 

## What our containers currently contain

All containers come as standard with the following: 
<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; 
-webkit-column-rule: none; -moz-column-rule: none; column-rule: none;">
    <div style="display: inline-block;">
        <p> h5py </p>
        <p> ipympl </p>
        <p> ipython </p>
        <p> ipywidgets </p>
        <p> jupyterlab </p>
        <p> jupyterlab_widgets </p>
        <p> jupyter_nbextensions_configurator </p>
        <p> matplotlib-base </p>
    </div>
    <br>
    <div style="display: inline-block;">
        <p> nodejs </p>
        <p> python-confluent-kafka </p>
        <p> pythreejs </p>
        <p> voila </p>
        <p> bqplot </p>
        <p> ipyvolume </p>
        <p> ipympl </p>
    </div>
</div>

      
      

| ------ | ----------- | ----------- | ----------- |
| Dockerhub name | trnielsen/jhub_py38_ikon21_nb | movingnorthwards/crispy | movingnorthwards/ |
| dockerfile | [link](https://github.com/trnielsen/Docker/tree/master/jhub38_dram_ikon21) | [link](https://github.com/moving-northwards/docker4pan-learning/blob/main/Crispy/Dockerfile) | [link](https://github.com/moving-northwards/docker4pan-learning/blob/main/SimEx/Dockerfile) |



## First time with docker

If you do not have any prior experience, this is not a problem. Here we will guide you through. 

1. Download and install docker following the instructions on [docker's website](https://docs.docker.com/get-docker/). Note that Mac and Windows users will install 'docker desktop', however this is not necessary for linux users as you can interact with docker purely through the terminal. 

2. Practice pulling one of our containers. 
```markdown
sudo docker pull moving-northwards/crispy 
```
(Linux users: If you wish to avoid typing sudo with each docker command you can become root with `sudo -i`.)

3. Try running the container on your own computer. This will help you understand how the containers work on our e-learning platform. 
```markdown
docker run -p 8888:8888 moving-northwards/crispy 
```
At the bottom of the output you will see a similar message to: 
```markdown    
    To access the notebook, open this file in a browser:
        file:///home/jovyan/.local/share/jupyter/runtime/nbserver-7-open.html
    Or copy and paste one of these URLs:
        http://29d5bca97b1d:8888/?token=8a93c688b03a17b597035daaf9d6b134e1465b04afafd717
     or http://127.0.0.1:8888/?token=8a93c688b03a17b597035daaf9d6b134e1465b04afafd717
```
Open one of the URls in your browser. You can then upload a Jupyter notebook which uses crispy as can be found here: [https://github.com/mretegan/crispy-pan-learning](https://github.com/mretegan/crispy-pan-learning). 
