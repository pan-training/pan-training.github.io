---
permalink: /docs/containers/
classes: wide
title: Our images
---

All our docker images are based on the [Jupyter base-notebook](https://hub.docker.com/r/jupyter/base-notebook/) from docker stacks. If you look at their [dockerfile](https://github.com/jupyter/docker-stacks/blob/master/base-notebook/Dockerfile), you can see they start from the [ubuntu:focal](https://hub.docker.com/_/ubuntu?tab=tags) image and install [Miniforge](https://conda-forge.org/#about). 

We currently have three docker images in use on the e-Learning platform. We are in the process of updating these and adding new ones.

## What our images currently include

As well as the usual modules that come with Miniforge all our images include the following packages: 
<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; 
-webkit-column-rule: none; -moz-column-rule: none; column-rule: none;">
    <div style="display: inline-block; list-style-type:none;">
        <li> h5py </li>
        <li> ipython </li>
        <li> ipywidgets </li>
        <li> jupyterlab </li>
        <li> jupyterlab_widgets </li>
        <li> jupyter_nbextensions_configurator </li>
        <li> matplotlib-base </li>
    </div>
    <br>
    <div style="display: inline-block; list-style-type:none;">
        <li> nodejs </li>
        <li> python-confluent-kafka </li>
        <li> pythreejs </li>
        <li> voila </li>
        <li> bqplot </li>
        <li> ipyvolume </li>
        <li> ipympl </li>
    </div>
</div>
<br>

We also include [nbgitpuller](https://jupyterhub.github.io/nbgitpuller/) along with other Nbextensions. 

Here are the containers we are currently using:

| ------ | ----------- | ----------- | ----------- |
| Docker Hub| [trnielsen/jhub_py38_ikon21_nb](https://hub.docker.com/r/trnielsen/jhub_py38_ikon21_nb) | [movingnorthwards/crispy](https://hub.docker.com/r/movingnorthwards/crispy) | [movingnorthwards/carstensimex](https://hub.docker.com/r/movingnorthwards/carstensimex) |
| dockerfile | [link](https://github.com/trnielsen/Docker/tree/master/jhub38_dram_ikon21) (image needs updating) | [link](https://github.com/moving-northwards/docker4pan-learning/blob/main/Crispy/Dockerfile) | [link](https://github.com/moving-northwards/docker4pan-learning/blob/main/SimEx/Dockerfile) |
| Specific applications installed | [McStas](https://www.mcstas.org/) [McXtrace](https://www.mcxtrace.org/) [McStasscript](https://mads-bertelsen.github.io/)  [SasView](https://www.sasview.org/) [SCIPP](https://scipp.github.io/) | [CrisPy](https://www.esrf.fr/computing/scientific/crispy/) | [SimEx](https://simex.readthedocs.io/en/latest/) |
