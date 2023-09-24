# Docker Essentials

## Overview
  - Introduction To WebApps and Containers
  - Docker and DockerFiles
  - Docker Images and Containers
  - Docker Networks
  - Storage
  - Docker Compose
  - Docker Swarm
    
## What is a Web-app ( Web Application ) ?
  - A Web Application is any program that is accessed over a network connection using any protocol such as HTTP, etc, rather than using an application existing within a devices memory.

### How to make a Web App
  - On a Over View we can say that there are 3 stages to the process of making Web Apps
    * Make it or Build it in a Suitable Environment.
    * Wrap or Pack it with necessary support and requirments to deliver it to the intended consumer.
    * Host it a server for others to access it.

### Containers
  - Containers are an abstraction at the Application Layer that packages codes and dependencies together
  - it means instead od just shipping the application , it also ship the runtime environment along with the application
  - i.e. they contain the application code and dependencies ( not only third party libraries but also OS related dependencies )

### VM's vs Containers
  - VM's require Hypervisor ( for ex : HyperV ) on top of hardware Infrastructure ( Type 1 Hypervior as they do not require Host OS , Type2 Hypervior which requires Host OS ) , over which Guest OS are provisioned and they acquire their isolated Virtual Environment
  
  - Containers do not require guest OS , Container runtime environment ( Software which manages and runs Containers ex: Docker ) is used instead of HyperVisor which is present on Host OS
    - ![Screenshot (509)_1](https://github.com/SurajKande/Docker/assets/37841586/2999f742-aa7e-455d-a5e9-931d543bcca5)
  
  - Containers contain application code as well as dependencies , which include OS level related dependencies as well.
    - for example as all linux variants contain the same Linux Kernal more or less ( The kernel is the most important part of the operating system. It is the primary interface between the hardware and the processes of a computer ) its pointless in duplicating the same set of files over and over in multiple VM's if all containes can just access them in their own isolated environment
    - the Files which are uncommon, containers contain them along with the application
  
  - The Process of creating Containers and running them are done by same Container runtime environment , there will be no conflict of environment
  - hence Containers can attain same level of isolation as VM's , while sharing the resources to the host OS instead of duplicating
    - Consumes less storage and memory
    - Easier and faster to ship
    - if they work on one machine, they work on all machines ( as all dependencies are packed into the container )
    - cost efficient and easy to scale
    - possible to eliminate data loss and downtime

### Docker
  - An Open platform for developers and system admins to build, ship and run containerized applications
  - Most widely used Containerization platform ( another example for Containerization platform is rocket )
  - Hence has a good Community support and has large amount of 3rd party application support
