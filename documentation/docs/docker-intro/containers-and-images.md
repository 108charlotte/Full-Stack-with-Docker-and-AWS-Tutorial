---
sidebar_position: 2
---

# Containers and Images
The official Docker website defines a container as: 

:::info
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another ([article link](https://www.docker.com/resources/what-container/))
:::

Essentially, a container holds everything necessary to run an application <u>except for a kernel</u>, which it shares with the host computer. 

It also defines container images: 

:::info
A Docker container image is a lightweight, standalone, executable application that includes everything needed to run an application: code, runtime, system tools, system libraries, and settings ([article link](https://www.docker.com/resources/what-container/))
:::

Essentially, this means that container images allow you to create containers on your local machine when you execute them. 

<figure>
![The process going from a dockerfile to a docker container](./img/dockerfile-to-image-to-container.png)
    <figcaption>
        A docker container image is created from a dockerfile (more about this [here](./dockerfiles.md)). Running an image produces a container! (image from [this CTO.ai article](https://cto.ai/blog/docker-image-vs-container-vs-dockerfile/))
    </figcaption>
</figure>

:::tip
You use a container image to create a container on your local machine. You can get images from various online libraries, including [Docker Hub](./docker-hub.md) and [Amazon ECR](https://gallery.ecr.aws/), or create your own! 
:::

