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
$hello-world: git clone https://github.com/jodeh/dockerizing-nodejs.git
```

Now we'll build the docker and check if the image was created.
```
$hello-world: docker build . -t <your username>/node-web-app
$hello-world: docker images
```
Last but not least we will run the image, we're going to map the port of 49160 to the port specified in the Dockerfile 8080. As well as we will run it in the [detached mode](https://www.freecodecamp.org/news/docker-detached-mode-explained/) which will run it in the background.
```
$hello-world: docker run -p 49160:8080 -d <your username>/node-web-app
```
Finally it's time for testing our work, you can basiclly go to your localhost with the port number we used **49160** or you can use this command.
```
$hello-world: curl 0.0.0.0:49160
```
