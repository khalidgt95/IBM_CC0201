# Containers
- When running different applications, it becomes important to isolate them and give them dedicated resources
- If everything is running on a single machine, then that machine becomes a single point of failure
- To isolate user space instances, we use the concept of containers
- Each container or application space is independent from each other, meaning that they do not know about other's existence
- This segregation helps to isolate different components incase one of them fails
- These containers all use the same underlying kernel who manages them
## Why do we need containers?
- As more and more softwares shift to the cloud, there arises a very unique problem; How to write code on my laptop that can also work in a cloud hosted environment with different OS and hardware specifications?
- Sepcifically, given a set different services communicating with each other, how make them robust with ever changing software landscape?
- The following picture gives a visual representation of the problem faced by developers <br><br><p align="center"><img src="https://www.docker.com/blog/wp-content/uploads/2013/08/the_challenge.jpg" align=""></p>
- To solve the above mentioned problems, developers can use <b>"Containers"</b> to wrap their application in such a way that everything required for the component is bundled together all in a single place. The following image illustrates this concept: <br><br><p align="center"><img src="https://courses.edx.org/assets/courseware/v1/ab813032f150e0d74d9016b2e8a55ed3/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Docker_Container.jpeg" align=""></p>
## Basic Concepts
- A container is created from an <b>Image</b>. This image contains all the instructions necessary to start and run the container.
- Once a container is started, the OS creates a separate namespace for it and isolates it from other processes
- An image is like a blueprint which instructs how to create a container. Multiple containers can be created from a single image
- For the OS, a container is just like any other program
- A container has two important concepts which are mentioned below:
    ### 1. <b>Namespaces</b>
    - This is an abstraction layer in which all the system's resources reside.
    - It behaves like a virtual isolation
    - Each process lives inside a namespace
    - To the running process, it can only see the resources assigned to it in it's namespace
    - There are 6 types of namespaces
    ### 2. <b>Cgroups</b>
    - It controls how much resources a process can use
    - Organizes and manages the resource allocation
## Container runtime
- A container by itself is nothing but a collection of different low level kernel resources bundled together into a single object
- A container runtime allows to bundle these pieces together in a simple and reusable manner
- This runtime follows industry standard, which means that it is portable across different infrastructure and OS
- Container runtime abstracts the host system specific information and provides a consistent view across all hosts
- There are two specifications which govern the use of container runtimes:
    <br><br>
    ### 1. <b>Open Container Initiative(OCI)</b>
    - Define a set of protocols and standards on how to access the underlying host resources by the runtime
    ### 2. <b>Container Runtime Interface(OCR)</b>
    - Kubernetes also requires plumbing code to interact with the container runtime
    - Since there are a lot of container runtimes in the market, therefore to allow kubernetes to support all of these they decided to create an interface which runtimes can support
    <br><br>
- Some of these runtimes are listed below:
    ## 1. runC
    - runC is a container runtime created by Docker
    - It takes care of all the plumbing details required for a container to interact with the Kernel's system resources
    - Features of runC include native support for different computing architectures such as Arm, Intel, Qualcomm, DPDK, Windows
    ## 2. containerd
    - It can be thought of as a wrapper on top of runC
    - The idea is that runC offers direct communication with the Kernel. These include native syscalls or OS specific functionality
    - To create an abstraction from these low level concepts, containerd was created
    - This image offers a nice overview of where containerd fits:
    <br><br><p align="center"><img src="https://i0.wp.com/www.docker.com/blog/wp-content/uploads/974cd631-b57e-470e-a944-78530aaa1a23-1.jpg?w=906&ssl=1" align=""></p>
    - It works as a separate process, providing the bridge between Docker and runC
    - It is OCI-compliant, meaning that other conainer technologies can also use it
    - It provides APIs to manage, create and execute any container with the host system
    ## 3. rkt
    - It is another runtime container runtime provided by Redhat
    - Difference from docker is that it does not have any daemon like docker run, so each container is independent
    - This project is unfortunately archived and not used anymore
    ## 4. CRIO-O
    - It is an implementation of CRI
    - Alternative to docker for kubernetes runtime
    - This link gives a nice architectural overview:
    <br><br><p align="center"><img src="https://cri-o.io/assets/images/architecture.png" align=""></p>
## Containers vs VMs
- In a VM, for each instance you spin up a dedicated VM for this. These VMs are running on a host machine and are managed by a Hypervisor
- In Containers, each instance sits on top of an existing host, sharing the underlying host kernel's resources but logically separated
- This image gives a nice architectural overview:
    <br><br><p align="center"><img src="https://wiki.aquasec.com/download/attachments/2854029/docker-birthday-3-intro-to-docker-slides-18-638.jpg?version=1&modificationDate=1515522843003&api=v2" align=""></p>
## Docker
- It is a technology company which offers Docker containers as their product
 <br><br><p align="center"><img src="https://wiki.aquasec.com/download/attachments/2854029/Docker.JPG?version=1&modificationDate=1515349366681&api=v2" align=""></p>

## Benefits of containers
- Fast to deploy
- Elastic scaling
- Less memory footprint against VMs
- Portable across different environments
# Project Moby
- Created by docker and allows to create a container system by the user himself
- User can create custom container systems similar to docker
- Since container systems need a lot of plumbing code to acces host's resources, therefore moby provides a set of APIs so that the user does not have to do these tasks

