# Cloud computing

## Advantages of cloud computing

1. Organizations can be more Agile (Faster delivery cycles)
2. Cost reductions since companies don't need a dedicated team to manage the servers
3. Device and location independence
4. Multitenancy
5. Performance due to elastic nature of cloud
6. Availability because of built-in distributed fault tolerance 
7. Productivity due to easier sharing of resources
8. Security
9. Pay as you go model

## Models of Cloud computing
 
<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Cloud_computing_layers.png" align=""></p>


## 3 possible strategies to deploy a cloud enviroment

1. Private
2. Public 
3. Hybrid

<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/8/87/Cloud_computing_types.svg" align=""></p>

## Virtualization

- Creating a vritual copy/instance of something which exists physically
- Almost everything(RAM, CPU, HDD, Network) can be virtualized

#### <b>Hypervisor</b>
- They are used to create VMs
- It runs on a host(e.g. personal) machine
- There are 2 categories of hypervisors
    - <b>Type-1 Hypervisor </b>
        - Runs directly on the hardware wihtout installing any OS
        - Examples are Microsoft Hyper-V, VMware ESXi, Xen, IBM z/VM, AWS Nitro, KVM, bhyve
    - <b>Type-2 Hypervisor </b>
        - Runs on an OS
        - Typically used by user
        - Examples are VMware Workstation, VirtualBox, KVM, bhyve


## KVM
- A kernel module which turns the Linus OS into a hypervisor
- Built-in in the linux kernel
- Allows nesting of OS
<p align="center"><img src="https://upload.wikimedia.org/wikipedia/commons/4/40/Kernel-based_Virtual_Machine.svg" align=""></p>

## Vagrant
- Automate VMs management by providing an end-to-end lifecycle management utility
- Has two components
    1. <b>Provisioners</b>
        - Tools which allow to customize the configuration of virtual environments E.g. Puppet, Ansible. Chef
    2. <b>Providers</b>
        - Services which are used to creat virtual environments. E.g. Docker, VirtualBox, Hyper-V
- It provides a <b>Vagrantfile</b> which describes how the Vms should be configured and prvisioned. There can be only <b>1</b> vagrantfile per project
- 

