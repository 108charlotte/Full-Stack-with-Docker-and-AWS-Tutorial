---
sidebar_position: 1
---

# What is Docker? 
Docker is a containerization platform, similar to a virtual machine (VM) except that it is lighter-weight by sharing the kernel of its host computer's operating system. 

:::info
A kernel is the part of the operating system which delegates resources and manages the execution of applications, and manages the communication between different processes. It also controls file system management and networking. 
:::

To understand this, let's first look at how virtual machines operate on a computer. 

<figure>
![Virtual machines running without Docker](./img/virtual-machines-docker.avif)
<figcaption>Each application runs in a virtual machine which has its own "Guest Operating System," which is computationally expensive (image from [this Docker tutorial](https://www.docker.com/resources/what-container/) on containers and VMs)</figcaption>
</figure>

Now, compare that to how containerized applications run on Docker: 

<figure>
![Separate containerized applications running on Docker](./img/containerization-with-docker.avif)
<figcaption>Docker allows containers to use the host OS's Linux kernel rather than their own guest OS (image from [this Docker tutorial](https://www.docker.com/resources/what-container/) on containers and VMs)</figcaption>
</figure>

Giving containers access to the kernel provides the functionality for applications to set up only the configurations they need, making containerization with Docker much more lightweight than creating separate virtual machines for each application.  