# Learn Kubernetes
 A Simple Guide to K8S

### What is Kubernetes 

(Definition by Offcial Kubernetes Documentation)

Kubernetes is a portable, extensible, open-source 
platform for managing containerized workloads and 
services, that facilitates both declarative 
configuration and automation.

### K8S Features

* Container Orchestration

    The primary purpose of Kubernetes is to dynamically manage containers across multiple host systems.

* Application Reliability

    Kubernetes makes it easier to build reliable, self-healing, and scalable applications.

* Automation

    Kubernetes offers a variety of features to help automate the management of your container apps.

### Kubernetes Architectural Overview

#### Control Plane

The control plane is a collection of multiple components responsible for managing the cluster itself globally. Essentially, the control plane controls the             cluster. Individual control plane components can run on any machine in the cluster, but usually are run on dedicated controller machines.

* Components of Control Plane

    1. kube-api-server
       
       kube-api-server serves the Kubernetes API,the primary interface to the control plane and the cluster itself. When interacting with your Kubernetes cluster, you        will usually do so using the Kubernetes API.
       
    2. etcd
       
       Etcd is the backend data store for the Kubernetes cluster. It provides high-availability storage for all data relating to the state of the cluster.
       
    3. kube-scheduler
       
       kube-scheduler handles scheduling, the process of selecting an available node in the cluster on which to run containers.
       
    4. kube-controller-manager
    
       kube-controller-manager runs a collection of multiple controller utilities in a single process. These controllers carry out a variety of automation-related            tasks within the Kubernetes cluster.
       
    5. cloud-controller-manager
       
       cloud-controller-manager provides an interface between Kubernetes and various cloud platforms. It is only used when using using cloud-based resources alongside        Kubernetes.
 
 ##### Nodes
 
Kubernetes Nodes are the machines where the containers managed by the cluster run. A cluster can have any number of nodes. Various node components manage              containers on the machine and communicate with the control plane.

* Componenets of node

    1. kubelet
       
       Kubelet is the Kubernetes agent that runs on each node. It communicates with the control plane and ensures that containers are run on its node as instructed by        the control plane. Kubelet also handles the process of reporting container status and other data about containers back to the control plane.
       
    2. container runtime
       
       The container runtime is not built into Kubernetes. It is a separate piece of software that is responsible for actually running containers on the machine.              Kubernetes supports multiple container runtime implementations. Some popular container runtimes are Docker and containerd.
       
    3. kube-proxy
       
       kube-proxy is a network proxy. It runs on each node and handles some tasks related to providing networking between containers and services in the cluster.

