---
permalink: /docs/overview/
classes: wide
title: Overview
---

Jupyter notebooks are great for demonstrating good data reduction and analysis along with modeling and simulation techniques. They can also be used to virtually explore instruments at large-scale facilities by using python-based ray-tracing applications (e.g. [McStas](https://www.mcstas.org/)).   

On PaN e-Learning you can link a JupyterHub instance to a course that runs on servers at the [European Spallation Source](https://europeanspallationsource.se/). Crucially, this means scientists and students can _have a go_ without installing applications or Jupyter on their computer. They do not even need to have prior python experience. 

{% include note.html content="We will soon be moving to JupyterLab." %}
### How it works 

A [docker](https://docs.docker.com/get-started/overview/) container is launched from the course page, which runs on a [kubernetes](https://kubernetes.io/) cluster. The docker container is accessed through a new browser tab that displays the standard JupyterHub. When the container launches, [nbgitpuller](https://jupyterhub.github.io/nbgitpuller/) clones the GitHub repository that contains your Jupyter notebooks into the home directory. Students can open, execute and edit the notebooks as though it were running on their own computer. 


This is very similar to how [binder](https://mybinder.readthedocs.io/en/latest/) works. The advantage over binder is that:
- Compute resources can be tailored to your course.  
_Running a large simulation on binder would take a **very** long time. Although is unlikely that the binder maximum number of simultaneous users for a given repository (100) would be exceeded, we prefer to be sure._
- Access to the container is controlled via the moodle authentication.   
_Hence only people with an account enrolled onto a specific course can launch a container._
- You can integrate other material such as notes, videos, slides and quizzes on the course page. 

We currently have three docker images in use on the e-Learning platform. We are in the process of updating these and adding new ones. Check out [our images]({% link docs/containers.md %}).  

### Requirements

1. What the student interacts with must be in the form of a Jupyter notebook.
2. Your notebooks and additional files must be on a public GitHub repository.

{% include note.html content="The ***entire*** repository you provide will be cloned, not just selected notebooks/folders. However it does not have to be the main branch." %}


### Desktop software 

We are also in the process of developing containers for applications that require the more traditional desktop GUI (similar to how one might use a virtual machine). The first two will be for the [McStas GUI application](https://www.mcstas.org/) and [Oasys](https://www.aps.anl.gov/Science/Scientific-Software/OASYS). To find out more about how this will work, check out:
- [https://github.com/jupyterhub/jupyter-remote-desktop-proxy](https://github.com/jupyterhub/jupyter-remote-desktop-proxy)
- [https://github.com/yuvipanda/jupyter-desktop-server](https://github.com/yuvipanda/jupyter-desktop-server)



