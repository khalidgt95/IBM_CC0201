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
- 
