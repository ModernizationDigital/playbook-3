---
layout: page
title: 'How do they work'
---

Containers in the cloud
animated diagrams

### Monolith

To understand how containers work, let's look at an app in a monolith environment [column 1 in the image below]. Right now your app may sit in a physical server in your office. If you move it there are many things to reconfigure. Dependent on many things, it's becoming obsolete, and it can break easily. This can be thought of as a 1 to many relationship. One app connected to many things. To run your app this way you need physical infrastructure. This is IAAS
![ApplicationEnvironments]({{site.baseurl}}/images/appEnvironments.png) 

### Virtual Machines
A virtual machine [column 2 in the image above] is a computer file, that behaves like an actual computer. A computer within a computer. You can have many VM's on one computer. Each is its' own little computer. However a VM is very heavy, it needs a full configuration, it can be gigabytes in size, it's dependent on a physical machine, and it can be difficult to move. It is still running on your monolith infrastructure. A Virtual Machine is still a one to many relationship and IAAS.  

### Containers
A container is where things start to change [column 3 in the image above]. It is a standardized package capable of running an application with out the full operating system. It can be run on any platform. When you run a container, you don't install anything!  It doesn't need servers, or physical hardware. It's size is megabytes, and this makes it very portable. This app state is considered a one to one relationship. It only needs itself. Serverless. 

Containers are used to build blocks, which help in producing operational efficiency, version control, developer productivity and environmental consistency. All of this assures the user of reliability, consistency, and speed regardless of the distributed platform. The infrastructure is enhanced since it provides more control over the granular activities on resources. Using a container allows you to take advange of the cloud capabilities of storage, information security, availability and elasticity.

### Serverless
Now it becomes a little harder do understand. It's just code. And somehow the internet knows how to organize it. And it makes everything faster and more seemless. [column 4 in the image above]

### Saas