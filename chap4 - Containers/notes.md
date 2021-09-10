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

    ### 2. Cgroups
    - 