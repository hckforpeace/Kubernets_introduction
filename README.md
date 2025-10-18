# Kubernetes

## What is 

Kubernetes is a portable, extensible, open source platform for managing containerized workloads and services, that facilitates both declarative configuration and automation. It has a large, rapidly growing ecosystem. Kubernetes services, support, and tools are widely available.

# Key components

![Kubernetes diagram](https://kubernetes.io/images/docs/components-of-kubernetes.svg)

### Core Components

A Kubernetes cluster consists of a control plane and one or more worker nodes. Here's a brief overview of the main components:

### Control Plane Components 

Manage the overall state of the cluster:

##### kube-apiserver
 The core component server that exposes the Kubernetes HTTP API.

##### ketcd
Consistent and highly-available key value store for all API server data.

##### kube-scheduler
Looks for Pods not yet bound to a node, and assigns each Pod to a suitable node.

##### kube-controller-manager
Runs controllers to implement Kubernetes API behavior.

##### cloud-controller-manager (optional)
Integrates with underlying cloud provider(s).


### Node Components
Run on every node, maintaining running pods and providing the Kubernetes runtime environment:

#### kubelet
Ensures that Pods are running, including their containers.

#### kube-proxy (optional)
Maintains network rules on nodes to implement Services.

#### Container runtime
Software responsible for running containers. Read Container Runtimes to learn more.
