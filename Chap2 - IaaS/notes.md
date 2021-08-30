# IaaS - Infrastructure As A Service

- A cloud service model that provides on-demand physical and virtual computing resources (E.g. storage, compute, network, firewall, load balancers)
- Offered by all the major cloud providers

## 1. Amazon EC2 (Amazon Elastic Compute Cloud)
- This is the core of Amazon's IaaS model
- It is a set of Vms running on top of hypervisors. These hypervisors are Type-1 hypervisors such as KVM, Xen, Nitro
- When a user wants to provision an EC2 instance, he has the choice of managing different aspects of the machine such as OS, Hardware resources, firewall settings, etc.
- <b>Amazon Machine Images (AMI)</b> are a set of predefined OS images which provide basic OS functions (E.g. UI, basic softwares) that can be used to initialize the machine
- <b>Instance Types</b> are the different categories of VMs based on their hardware settings. 
## 2. Azure Virtual Machine
- Allows the users to provision VMs from the web or [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview)
- It allows to control the resources of the VMs such as Network, compute, Storage and so on
- Benefits include easy-to-use UI, automation, cost-effective and connection to other azure services

## 3. Digital Ocean Droplet
- One of the leading cloud service providers
- The instances are called <b>"Droplets"</b>
- They use KVM as their underlying hypervisor

## 4. Google Compute Engine (GCP)
- IaaS platform offered from Google
- They use KVM as their hypervisor
- Offers the same benefits as other cloud providers

## 5. IBM Cloud virtual servers
- They offer a mixture of public, private and hybrid cloud stacks
- Biggest advantage is that users can choose a number of different hypervisors such as XenServer, VMware or Hyper-V hypervisors
- Same benefits as other cloud providers, but price comes more on the end of the curve

## 6. Oracle cloud compute Virtual Machines
- Capable of supporting nested virtualizations
- Also offers ARM based compute
- Provides standard as well as dense IO/ High-performance instances. 

## 7. Openstack
- With openstack, you can basically become a cloud provider yourself by setting up an IaaS on bare metal machines
- This software allows you to do everything a normal cloud offering company, from provisioning VM instances to managing them
- This project was a joint effort between NASA and Rackspace
- It contains a number of components which are dedicated to a certain feature or functionality such as Network, Storage, Orchestration and so on
- It is open-source and supports most technological domains such as Data Science and Machine Learning
