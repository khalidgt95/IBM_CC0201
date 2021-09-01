# Platform as a Service (PaaS)
- It is a cloud serivce model which can be defined a layer below the IaaS service
- Here, a user does not need to manage any infrastructure related problems or installing components or bare metal machines
- Instead, the managemnent of the underlying infrastructure is abstracted
- Users can take any machine and start to develop their applications without worrying about the internal details of how everything is managed (Hypervisors, networking layers, storage, etc.)
- Due to this abstraction, application developers can quickly setup their working environments
- Users can develop, run and manage their applications
- The article from [IBM](https://www.ibm.com/cloud/learn/paas) provides a very good explanation about this concept
- Most cloud providers such as AWS, Azure and GCP provide PaaS solutions.
- Users can also deploy their own PaaS infrastructure using the following tools

## 1. Cloud Foundry
- Open source PaaS solution geared towards developers to deploy their applications quickly and easily with some commands
- Supports a lot of popular programming languages
- Can be deployed on any IaaS platform such as AWS, GCP or Azure
- Makes it easy for developers to use microservice architecture
- Advantages include auto-scaling, logging, dynamic routing, portability, etc
- Has two runtimes called "Cloud Foundry Application Runtime" and "Cloud Foundry Container Runtime"
- Both of these tools are managed by [BOSH](https://bosh.io/docs/)
- This tool can work on any IaaS platform
