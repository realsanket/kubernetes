# kubernetes

This repository contains documentation and code samples for using Kubernetes. This is good for beginners who want to learn Kubernetes.

In this repository, you will have a understanding of Kubernetes and how to use it. You will also learn how to deploy a Kubernetes cluster on your local machine using Minikube.


## What is Orchestration?

Orchestration is the automated configuration, coordination, and management of computer systems and software. It helps to manage complex computer systems and services with ease. It is used to manage the lifecycle of containers. It is used to deploy, scale, and manage containerized applications.

## Why do we need Orchestration?

Orchestration is needed to manage the lifecycle of containers. It is used to deploy, scale, and manage containerized applications. It is used to manage complex computer systems and services with ease. It helps to manage complex computer systems and services with ease.

## What is Kubernetes?

Kubernetes is an open-source container orchestration tool developed by Google. It is used to manage the lifecycle of containers. It is used to deploy, scale, and manage containerized applications. It is used to manage complex computer systems and services with ease.

## Why do we need Kubernetes?

Kubernetes is needed to manage the lifecycle of containers. It is used to deploy, scale, and manage containerized applications. It is used to manage complex computer systems and services with ease. It helps to manage complex computer systems and services with ease.

## Terminologies

- **Node**: A node is a worker machine in Kubernetes. It may be a VM or physical machine, depending on the cluster. Each node has the services necessary to run pods and is managed by the master components. The services on a node include Docker, kubelet, kube-proxy, and a container runtime.
- **Cluster**: A cluster is a set of nodes grouped together. One of these nodes is elected as the Master node, and the others are Worker nodes. The Master node manages the cluster and the Worker nodes host the running pods.
- **Master**: A master is a node that controls the cluster. A cluster can have multiple masters for high availability. The master watches for changes on the nodes and pods and makes changes to bring the cluster’s current state to the desired state.
![Alt text](image.png)

## Components of Kubernetes

- **API Server**: The API server is a key component and serves the Kubernetes API using JSON over HTTP, which provides both the internal and external interface to Kubernetes. The API server processes and validates REST requests and updates state of the API objects in etcd, thereby allowing clients to configure workloads and containers across Worker nodes.

- **etcd**: etcd is a distributed key-value store that is used to store the cluster state. The Kubernetes master writes the cluster state to etcd. If the master crashes, it can read the cluster state from etcd.

- **Scheduler**: The scheduler is a key component and watches for newly created pods that have no node assigned. For every newly created pod, the scheduler selects an appropriate node based on the resource requirements of the pod and the available resources on the node.

- **Controller**: A controller is a key component and runs controllers that are responsible for different functions. These controllers include the replication controller, endpoints controller, namespace controller, and service accounts controller.

- **Container Runtime**: The container runtime is the software that is responsible for running containers. Kubernetes supports several container runtimes: Docker, containerd, CRI-O, and any implementation of the Kubernetes CRI (Container Runtime Interface).

- **Kubelet**: The kubelet is a key component and runs on each Worker node. It communicates with the API server and manages the containers running on the node. It also takes care of node-level operations such as starting pods and containers, and health checks.
![Alt text](image-1.png)

## Master vs Worker Node

- **Master Node**: The master node is responsible for managing the Kubernetes cluster. It runs the Kubernetes control plane processes, including the API server, scheduler, and controller manager. The master node communicates with worker nodes to schedule and run containers on them.

- **Worker Node**: The worker node is responsible for running the containers. It runs the kubelet process and is managed by the master node. The worker node communicates with the master node using the Kubernetes API, which the master node exposes.

### How you will determine which node is master and which node is worker?

Worker node have container runtime and kubelet installed on it.
Master node have etcd, kube-apiserver,kube-controller-manager,kube-scheduler installed on it.

![Alt text](image-2.png)

## Kubectl

Kubectl is a command-line tool that is used to deploy and manage applications on Kubernetes. It is used to view and manage components in a Kubernetes cluster. It is used to view and manage the state of Kubernetes objects, such as pods, namespaces, deployments, and services.

![Alt text](image-3.png)

