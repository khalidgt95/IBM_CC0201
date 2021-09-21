# Micro OSes for containers
- Micro OSes are specially designed for containers since they contain the minimal packages and services required to run them the OS
- All extra stuff such asGUI, apps and 3rd party services are not present which makes it exteremely light weight
- Some of the most common Micro OSes are Alpine Linux, Ranches OS, Atomic Host, Fedora Core OS and Ubuntu core
- The following figure presents a nice explanation:

<p align="center"><img src="https://courses.edx.org/assets/courseware/v1/8a902583b0493f78bc5135ddbe4f20e3/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Micro_OSes_for_Containers_updated.png" align=""></p>

- Some of the details of these Micro OSes are explained is section below:
## 1. Alpine Linux
- Independent and open-source Micro OS Linux distribution with simplicity, security and resource efficiency in mind
- Uses it's own package manager called "apk"
- 8 MB per container, requires around 130MB for storage volume
- Three modes for runtime
    ## 1. Diskless Mode
    - Entire system runs on RAM, which makes it exteremely fast
    ## 2. Data Mode
    - Mostly runs from RAM, but also loads <b>swap</b> storage and <b>var</b> directories on the volume
    - Useful in situations where user-data exceeds RAM size 
    ## 3. sys Mode
    - Traditional hard-disk install
- Benefits of Alpine Linux include small size, increased security as well as portability across different hardware platforms such as Raspberry Pi
## 2. Fedora CoreOS
- Optimized to work with Kubernetes and designed to run containerized workloads
- Spin-off from CoreOS container linux, which was desgined as a container native OS
- Focuses on security
- Can run in a clustered as well as a container environment
- Can be launced on bare metal as well as PaaS environments
## 3. Rancher OS
- Another lightweight linux distribution, made entirely from containers
- Smallest footprint among all OSes since it needs to run only docker. All other features are pulled dynamically by docker
- Runs two separate docker instances, the first is docker daemon called <b>System Docker</b> which runs system containers such as <b>console</b>, <b>dhcp</b>, <b>syslog</b>
- The system docker daemon starts second docker daemon called <b>User Docker</b> that isolates system containers
- This means that user containers have no way to access these services
- The following picture explains this concept: <p align="center"><img src="https://courses.edx.org/assets/courseware/v1/fb5f9c500178d4fd6af74b1241ed05fa/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Figure_6.4-_RancherOS_Architecture.png"  align=""></p>
## 4. Ubuntu Core
- Lightweight version of ubuntu specifically for embedded devices
- Focuses more on security such as transactional updates, automated restore points and application snapshots
- Designed to run on bare-metal as well as hosted solutions
- Uses Apparmor and Seccomp for application security
- Uses snap as the software manager
- Integrates CI/CD pipeline
## 5. VMware Photon
- Provided by VMware and optimized for cloud-native applications
- Can be used on VMware vSphere as well as on cloud computing platforms
- Available in minimal as well as full version
- Photon OS comes from VMware and optimized for VMware products
- Uses yum-compatible package manager called Tiny DNF (tdnf)
- Supports Kubernetes and Mesos