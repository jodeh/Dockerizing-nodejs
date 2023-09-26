# Dockerizing-Nodejs
## Description
In this guide I'll build a Nodejs Hello World Web App using Docker for running the application. This guide will assume that you have already downloaded [Docker](https://docs.docker.com/engine/install/ubuntu/) and [Node](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04), if not, you can check the links to download them.
### How to build
First of all we will make a new directory where all the files would live.
```
$~: cd desktop
$desktop: mkdir hello-world
$desktop: cd hello-world
```
The next step, we will clone this repository which contains all the files we need.
```
$hello-world:git clone https://github.com/jodeh/dockerizing-nodejs.git
```
Now we'll build the docker and check if the image was created.
```
$hello-world:docker build . -t <your username>/node-web-app
# Confirm image created
$hello-world: docker images
```
