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
- Has two runtimes called "Cloud Foundry Application Runtime" (CFAR) and "Cloud Foundry Container Runtime" (CFCR)
- Both of these tools are managed by [BOSH](https://bosh.io/docs/)
- This tool can work on any IaaS platform. They are explained below:
    1. ###  <b>CFAR</b>
        * The CFAR platform manages the entire workflow of the application and provides the connections necessary for different services to work together
        - The following [link](https://docs.cloudfoundry.org/concepts/architecture/) provides details of the architecture of CFAR
    2. ### <b>CFCR</b>
        - Allows the users to deploy their applications present inside a container
        - Manages containers of a Kubernetes cluster
        - This Kubernets cluster is then controlled by BOSH
        - The following figure explains this concept clearly:
        <p align="center"><img src="https://storageconsortium.de/content/sites/default/files/Bildschirmfoto%202018-10-19%20um%2011.48.55.jpg" align=""></p>
        - As can be seen, BOSH and Kubernetes both work together. Kubernetes manages containers while BOSH manages machines on which Kubernetes is running
- ### <b>KubeCF</b>
    - [Kubernetes native](https://www.cloudfoundry.org/technology/kubecf/) version of CFAR, offering the benefits of Kubernetes combined with CFAR
    - Two main components: [Quarks](https://www.cloudfoundry.org/blog/quarks-using-cloud-foundry-operator/) and [Eirini](https://www.cloudfoundry.org/projects/#application_runtime_pmc-subproject-eirini)

## 2. OpenShift
- [OpenShift](https://www.redhat.com/en/technologies/cloud-computing/openshift) is an Open source PaaS solution provided by Red Hat
- Leading enterprise Kubernetes platform
- Works on popular IaaS solutions such as AWS, Azure or GCP
- Provides all the necessary technologies such as CI/CD, Monitoring all at one place
- Optimized for developers to quickly deploy application to Kubernetes using Source-to-Image (S2I) framework
<p align="center"><img src="https://www.tutorialspoint.com/openshift/images/openshift_container_platform_architecture.jpg" align=""></p>

## 3. Heroku
- Fully managed container-based cloud platform. This container is called <b>"dyno"</b>
- Dyno can be scaled on-demand
- It provides its own cloud environment, not connected to other cloud providers
- Allows developers to rapidly deploy their applications to the cloud without worrying about setting up other depencencies
- A file called [<b>"Procfile"</b>](https://devcenter.heroku.com/articles/procfile) contains all the commands which are executed on startup (similar to a dockerfile)
<p align="center"><img src="https://www.salesforce.com/content/dam/web/en_us/www/images/heroku/heroku-card-scalable-web-apps.jpg" align=""></p>
