---
permalink: /docs/containers/
classes: wide
title: Our images
---

All our docker images are based on the [Jupyter base-notebook](https://hub.docker.com/r/jupyter/base-notebook/) from docker stacks. If you look at their [dockerfile](https://github.com/jupyter/docker-stacks/blob/master/base-notebook/Dockerfile), you can see they start from the [ubuntu:focal](https://hub.docker.com/_/ubuntu?tab=tags) image and install [Miniforge](https://conda-forge.org/#about). 

We currently have three docker images in use on the e-Learning platform. We are in the process of updating these and adding new ones.

## What our images currently include

As well as the usual modules that come with Miniforge all our images build from [panbasic](https://hub.docker.com/r/stefanovdmsc/panbasic) include the following packages: 
<div style="-webkit-column-count: 2; -moz-column-count: 2; column-count: 2; 
-webkit-column-rule: none; -moz-column-rule: none; column-rule: none;">
    <div style="display: inline-block; list-style-type:none;">
        <li> h5py </li>
        <li> ipympl </li>
        <li> ipython </li>
        <li> ipywidgets </li>
        <li> jupyterlab </li>
        <li> jupyterlab_widgets </li>
        <li> jupyter_contrib_nbextensions </li>
        <li> matplotlib-base </li>
        <li> mkl </li> 
    </div>
    <br>
    <div style="list-style-type:none;">
        <li> nodejs </li>
        <li> python-confluent-kafka </li>
        <li> pythreejs </li>
        <li> voila </li>
        <li> bqplot </li>
        <li> ipyvolume </li>
        <li> scikit-learn </li>
        <li> nglview </li>
        <li> silx </li>
    </div>
</div>
<br>

We also include [nbgitpuller](https://jupyterhub.github.io/nbgitpuller/) along with other Nbextensions. 

Here are the containers we are currently using:


| ------- | ------- | -------- |
| Docker Hub | dockerfile | specific applications installed | 
| [stefanovdmsc/crispy](https://hub.docker.com/r/stefanovdmsc/crispy) | [link](https://github.com/pan-training/Docker/blob/main/crispy/Dockerfile) | [Crispy](https://www.esrf.fr/computing/scientific/crispy/) |
| [stefanovdmsc/dram](https://hub.docker.com/r/stefanovdmsc/dram) | [link](https://github.com/pan-training/Docker/blob/main/dram/Dockerfile) | [scipp](https://scipp.github.io/) [McStas](https://www.mcstas.org/) [McXtrace](https://www.mcxtrace.org/) [McStasscript](https://mads-bertelsen.github.io/)|
| easydiffraction | [link](https://github.com/pan-training/Docker/blob/main/easydiffraction/Dockerfile) | [easydiffraction](https://easydiffraction.org/) *not currently operational*  |
| [mccode/mcstas-2.7.1-3.1-scipp](https://hub.docker.com/r/mccode/mcstas-2.7.1-3.1-scipp) | [link](https://github.com/pan-training/Docker/blob/main/mcstasgui/Dockerfile) | [McStas](https://www.mcstas.org/) [scipp](https://scipp.github.io/) |
| [stefanovdmsc/oasys](https://hub.docker.com/r/stefanovdmsc/oasys) | [link](https://github.com/pan-training/Docker/blob/main/oasys/Dockerfile) | [OASYS](https://www.aps.anl.gov/Science/Scientific-Software/OASYS) |
| [stefanovdmsc/panbasic](https://hub.docker.com/r/stefanovdmsc/panbasic) | [link](https://github.com/pan-training/Docker/blob/main/panbasic/Dockerfile) | see above list |
| [stefanovdmsc/pyglotaran](https://hub.docker.com/r/stefanovdmsc/pyglotaran) | [link](https://github.com/pan-training/Docker/blob/main/[pyglotaran/Dockerfile) | [pyglotaran](https://pyglotaran.readthedocs.io/en/v0.5.1/introduction.html) |
| [stefanovdmsc/sasview](https://hub.docker.com/r/stefanovdmsc/sasview) | [link](https://github.com/pan-training/Docker/blob/main/sasview/Dockerfile) | [SasView](https://www.sasview.org/) | |
| [stefanovdmsc/scipp](https://hub.docker.com/r/stefanovdmsc/scipp) | [link](https://github.com/pan-training/Docker/blob/main/scipp/Dockerfile) | [scipp](https://scipp.github.io/) [scippneutron](https://scipp.github.io/scippneutron/) |
| [stefanovdmsc/simex](https://hub.docker.com/r/stefanovdmsc/simex) | [link](https://github.com/pan-training/Docker/blob/main/simex/Dockerfile) | [SimEx](https://simex.readthedocs.io/en/latest/) |





