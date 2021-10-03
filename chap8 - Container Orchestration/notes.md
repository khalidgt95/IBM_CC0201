# Container Orchestration
- When we consider enterprise applications, we see that there are multiple containers that need to be managed
- When we want to run containers in a multi-host environment, the following challenges arise:
    1. Managing multiple hosts and clusters
    2. Running containers on specifi hosts
    3. Communication between containers on multiple hosts or data centers
    4. Accessing storage which is present in another data center
    5. Name resolution of containers running separately
- To solve the above management problem of containers, we use <b>container orchestration</b> tools
- Container orchestration is a collective name for a set of services for container scheduling and cluster management
- Some popular tools for this are Docker Swarm, Kubernetes, Mesos marathon, Nomad and Amazon ECS
## Docker Swarm
- Orchestration technology provided by Docker
- Resembles closely a master slave architecture with multiple servers to provide fault-tolerance
- The following image illustrates this concept:
<p align="center"><img src="https://courses.edx.org/assets/courseware/v1/3d80bf4e48418dcd2fb5a3e38eb83a31/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Swarm_Cluster_Components.png" align=""></p> 

- Two main components can be seen here:
    1. <b>Swarm Manager Nodes</b> accepts user commands and manage the state of the cluster
    2. <b>Swarm Worker Nodes</b> executes the business logic workloads. They receive instructions from the manager 
- Some features of docker swarm are listed below:
    1. Native integration with docker tools because of the same company
    2. Provides HA and fault-tolerance
    3. Each service can be assigned number of tasks which are dynamically scaled based on the workloads
    4. Communication between nodes is done by using TLS
    5. Supports rolling updates. If something breaks then we can revert to previous stable state
## Docker Compose
- Allows us to define a set of containers in a system and how they interact with each other
- State of the system described in a YAML file
## Docker Datacenter
- Properitary solution provided by Docker for a hosted docker solution
- Uses the Container-as-a-Service (CaaS) model
<p align="center"><img src="https://courses.edx.org/assets/courseware/v1/a7f79f160ca545f97d5111eee0602510/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Fig_10.2_-_Docker_Datacenter.png" align=""></p> 
