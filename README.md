Repository for JupyterSiLK Docker image

Jupyter/SiLK is a [SiLK](https://tools.netsa.cert.org/silk/) training system that is built upon the [Jupyter](http://jupyter.org/) project and Jupyter Docker Demo Images (https://github.com/jupyter/docker-demo-images).  It brings all the power of the jupyter notebook project to netflow analysis in SiLK.  This includes the ability to create and share documents that contain live code, equations, visualizations and explanatory text.  The projects use cases are diverse, but include: becoming the de facto method for providing in person training, providing for an identical environment for self-driven training, and becoming the standard method for accessing the SiLK analysis tools

# Installation & Usage

```
docker run -p 8888:8888 --name jupytersilk certcc/jupytersilk
```

In your browser, navigate to the URL in the docker output:
It will be something like: http://localhost:8888/?token=

# Bring your own SiLK Repository

If you would like, you can mount your own repository in the /data directory in the container.

```
cd repo
docker run -v $PWD/repo:/data/repo:ro -p 8888:8888 certcc/jupytersilk
```

# Bring your own Notebooks

Mount notebook folder in the /home/jovyan/work directory in the container.

```
cd notebooks
docker run -v $PWD/notebooks:/home/jovyan/work:rw -p 8888:8888 certcc/jupytersilk
```

# Building a local docker image from included dockerfiles

If you would like to simply build a local docker image from the provided dockerfile, you can run the following command, with docker and docker-compose installed:

```
./build.sh
```

# License

Copyright 2017 Carnegie Mellon University. All Rights Reserved.

This material is based upon work funded and supported by the Department of Defense under Contract No. FA8702-15-D-0002 with Carnegie Mellon University for the operation of the Software Engineering Institute, a federally funded research and development center.

The view, opinions, and/or findings contained in this material are those of the author(s) and should not be construed as an official Government position, policy, or decision, unless designated by other documentation.
References herein to any specific commercial product, process, or service by trade name, trade mark, manufacturer, or otherwise, does not necessarily constitute or imply its endorsement, recommendation, or favoring by Carnegie Mellon University or its Software Engineering Institute.

NO WARRANTY. THIS CARNEGIE MELLON UNIVERSITY AND SOFTWARE ENGINEERING INSTITUTE MATERIAL IS FURNISHED ON AN "AS-IS" BASIS. CARNEGIE MELLON UNIVERSITY MAKES NO WARRANTIES OF ANY KIND, EITHER EXPRESSED OR IMPLIED, AS TO ANY MATTER INCLUDING, BUT NOT LIMITED TO, WARRANTY OF FITNESS FOR PURPOSE OR MERCHANTABILITY, EXCLUSIVITY, OR RESULTS OBTAINED FROM USE OF THE MATERIAL. CARNEGIE MELLON UNIVERSITY DOES NOT MAKE ANY WARRANTY OF ANY KIND WITH RESPECT TO FREEDOM FROM PATENT, TRADEMARK, OR COPYRIGHT INFRINGEMENT.

[DISTRIBUTION STATEMENT A] This material has been approved for public release and unlimited distribution.  Please see Copyright notice for non-US Government use and distribution.

Internal use:\* Permission to reproduce this material and to prepare derivative works from this material for internal use is granted, provided the copyright and “No Warranty” statements are included with all reproductions and derivative works.

External use:\* This material may be reproduced in its entirety, without modification, and freely distributed in written or electronic form without requesting formal permission. Permission is required for any other external and/or commercial use. Requests for permission should be directed to the Software Engineering Institute at permission@sei.cmu.edu.

\* These restrictions do not apply to U.S. government entities.
Carnegie Mellon® is registered in the U.S. Patent and Trademark Office by Carnegie Mellon University.

DM17-0973


