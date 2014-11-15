## Ubuntu Desktop (LXDE) Dockerfile


This repository contains **Dockerfile** of [Ubuntu Desktop (LXDE)](http://lxde.org/) for [Docker](https://www.docker.com/)'s [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu-desktop/) published to the public [Docker Hub Registry](https://registry.hub.docker.com/).


### Base Docker Image

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)


### Installation

1. Install [Docker](https://www.docker.com/).

2. Download [automated build](https://registry.hub.docker.com/u/dockerfile/ubuntu-desktop/) from public [Docker Hub Registry](https://registry.hub.docker.com/): `docker pull dockerfile/ubuntu-desktop`

   (alternatively, you can build an image from Dockerfile: `docker build -t="dockerfile/ubuntu-desktop" github.com/dockerfile/ubuntu-desktop`)


### Usage

    docker run -it --rm -p 5901:5901 -e USER=root dockerfile/ubuntu-desktop \
        bash -c "vncserver :1 -geometry 1280x800 -depth 24 && tail -F /root/.vnc/*.log"

Connect to `vnc://<host>:5901` via VNC client.
