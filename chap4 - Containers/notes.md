# Containers
- When running different applications, it becomes important to isolate them and give them dedicated resources
- If everything is running on a single machine, then that machine becomes a single point of failure
- To isolate user space instances, we use the concept of containers
- Each container or application space is independent from each other, meaning that they do not know about other's existence
- This segregation helps to isolate different components incase one of them fails
- These containers all use the same underlying kernel who manages them

## Why do we need containers?
- As more and more softwares shift to the cloud, there arises a very unique problem; How to write components/modules that can work across different OS/platforms without breaking?
- Sepcifically, given a set different services communicating with each other, how make them robust with ever changing software landscape?
- The following picture gives a visual representation of the problem faced by developers <br><br><p align="center"><img src="https://www.docker.com/blog/wp-content/uploads/2013/08/the_challenge.jpg" align=""></p>
- To solve the above mentioned problems, developers can use <b>"Containers"</b> to wrap their application in such a way that everything required for the component is bundled together all in a single place. The following image illustrates this concept: <br><br><p align="center"><img src="https://courses.edx.org/assets/courseware/v1/ab813032f150e0d74d9016b2e8a55ed3/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Docker_Container.jpeg" align=""></p>
