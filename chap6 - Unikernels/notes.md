# Unikernel
- Even in docker, we still have access to the full kernel space functions
- With Unikernels, we can select specific parts of kernel that are required by the application 
- In this technology, both the user app and the kernel are bundled into one single VM
- Due to this, they can directly run on a hypervisor
- They have the same address, hence they are also called <b>single-address-space machine</b>
- To build unikernels we can softwares such as [MirageOS](https://mirage.io) & Unik
## Benefits
- Faster boot time, since less packages to load
- Optimized resource utilization
- More secure than traditional VM
- Easily reporducible across different machines
## Types of Unikernels
- Unikernels can divided into two categories:
    ## 1. Specialized unikernels
    - Made with the latest tools and technologies.
    - Not backward and POSIX compatible
    - Examples are HaLVM, MirageOS & Clive
    ## 2. Fat Unikernels
    - Run unmodified applications
    - Examples are OSv & Drawbridge
## Comparison with Docker
- The following image shows the core difference between docker and Unikernels
- This illustrates how a lightweight VM looks like with the kernel and the application embedded together
<p align="center"><img src="https://courses.edx.org/assets/courseware/v1/49002a28650cb5cd1b750d8c9926ac60/asset-v1:LinuxFoundationX+LFS151.x+2T2020+type@asset+block/Fig8.2-SharedKernel-vs-Unikernel.png" align=""></p>