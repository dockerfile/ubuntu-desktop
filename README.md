## Ubuntu Desktop (LXDE) Dockerfile


This repository contains **Dockerfile** of [Ubuntu Desktop (LXDE)](http://lxde.org/) for [Docker](https://www.docker.io/)'s [trusted build](https://index.docker.io/u/dockerfile/ubuntu-desktop/) published to the public [Docker Registry](https://index.docker.io/).


### Dependencies

* [dockerfile/ubuntu](http://dockerfile.github.io/#/ubuntu)


### Installation

1. Install [Docker](https://www.docker.io/).

2. Download [trusted build](https://index.docker.io/u/dockerfile/ubuntu-desktop/) from public [Docker Registry](https://index.docker.io/): `docker pull dockerfile/ubuntu-desktop`

   (alternatively, you can build an image from Dockerfile: `docker build -t="dockerfile/ubuntu-desktop" github.com/dockerfile/ubuntu-desktop`)


### Usage

    docker run -it --rm -p 5901:5901 dockerfile/ubuntu-desktop

    USER=root vncserver :1 -geometry 1280x800 -depth 24

* Connect to desktop: `vnc://<host>:5901`
