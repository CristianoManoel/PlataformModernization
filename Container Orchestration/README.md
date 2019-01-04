# Container Orchestration: Learn paths, Best practices & References 

## Core concepts

1. **What is a container?**

    A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another. A Docker container image is a lightweight, standalone, executable package of software that includes everything needed to run an application: code, runtime, system tools, system libraries and settings.

    [Read More](https://www.docker.com/resources/what-container)

2. **What is container orchestration?**

    Container orchestration is all about managing the lifecycles of containers, especially in large, dynamic environments. Software teams use container orchestration to control and automate many tasks:

    * Provisioning and deployment of containers
    * Redundancy and availability of containers
    * Scaling up or removing containers to spread application load evenly *   across host infrastructure
    * Movement of containers from one host to another if there is a 
      shortage * of resources in a host, or if a host dies
    * Allocation of resources between containers
    * External exposure of services running in a container with the outside   world
    * Load balancing of service discovery between containers
    * Health monitoring of containers and hosts
    * Configuration of an application in relation to the containers running   it

3. **How does container orchestration work?**

    When you use a container orchestration tool, like Kubernetes or Docker  Swarm (more on these shortly), you typically describe the configuration of   your application in a YAML or JSON file, depending on the orchestration   tool. These configurations files (for example, docker-compose.yml) are    where you tell the orchestration tool where to gather container images (for    example, from Docker Hub), how to establish networking between containers,     how to mount storage volumes, and where to store logs for that container.   Typically, teams will branch and version control these configuration files    so they can deploy the same applications across different development and  testing environments before deploying them to production clusters.

    Containers are deployed onto hosts, usually in replicated groups. When it’s     time to deploy a new container into a cluster, the container orchestration  tool schedules the deployment and looks for the most appropriate host to     place the container based on predefined constraints (for example, CPU or    memory availability). You can even place containers according to labels or     metadata, or according to their proximity in relation to other hosts—all    kinds of constraints can be used.

    Once the container is running on the host, the orchestration tool manages   its lifecycle according to the specifications you laid out in the     container’s definition file (for example, its Dockerfile).

    The beauty of container orchestration tools is that you can use them in any     environment in which you can run containers. And containers are supported   in just about any kind of environment these days, from traditional    on-premise servers to public cloud instances running in Amazon Web Services    (AWS), Google Cloud Platform (GCP), or Microsoft Azure. Additionally, most     container orchestration tools are built with Docker containers in mind.

## Container management softwares

[Introduction to container orchestration: Kubernetes, Docker Swarm and Mesos with Marathon](https://www.exoscale.com/syslog/container-orchestration/)

[Best Container Management Software Comparative](https://www.g2crowd.com/categories/container-management)

## Trainings

[Scalable Microservices with Kubernetes (Udacity)](https://www.udacity.com/course/scalable-microservices-with-kubernetes--ud615)

[Introduction to Kubernetes (edX)](https://www.edx.org/course/introduction-to-kubernetes)

[Getting Started with Kubernetes (Pluralsight)](https://www.pluralsight.com/courses/getting-started-kubernetes)

[Hands-on Introduction to Kubernetes (Instruqt)](https://play.instruqt.com/public/topics/getting-started-with-kubernetes)

[Learn Kubernetes using Interactive Hands-on Scenarios (Katacoda)](https://www.katacoda.com/courses/kubernetes/)

[Certified Kubernetes Administrator Preparation Course (LinuxAcademy.com)](https://linuxacademy.com/linux/training/course/name/certified-kubernetes-administrator-preparation-course)

[Kubernetes the Hard Way (LinuxAcademy.com)](https://linuxacademy.com/linux/training/course/name/kubernetes-the-hard-way)

[Certified Kubernetes Application Developer Preparation Course (KodeKloud.com)](https://kodekloud.com/p/kubernetes-certification-course)

