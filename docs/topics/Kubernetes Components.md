tags: #kubernetes #k8s #overview

# Kubernetes Components

links: [[000 Index|Index]], [[300 Kubernetes MOC]]

---

# Components
![Image of kubernetes.io](_media/components-of-kubernetes.svg)
[source](https://kubernetes.io/docs/concepts/overview/components/)

We find out that a kubernetes installation has two main components. One is the control plane and the other are the nodes connected to the cluster. The control plane and the nodes aggregate different components of a kubernetes to form a cluster. This documentation here contains the minimal set of components which must be run to create a cluster. 
## Control Plane Components

The control plane is composed of following kubernetes components:

- kube-controller-manager
- cloud-controller-manager (only needed if the cluster is interacting with a cloud provider)
- kube-apiserver
- kube-scheduler
- etcd

The control plane can be run spanning multiple machines. The control plane is there to manage the nodes within a cluster.

### kube-controller-manager

A kubernetes cluster needs various controllers like a node controller, job controller and so one. For simplicity all controllers are contained in one binary and run as one process. The kube-controller-manager is responsible to manage all these controllers.

[More about controllers](https://kubernetes.io/docs/concepts/architecture/controller/)
### cloud-controller-manager

The cloud-controller-manager is the only component of the minimal setup which is optional. The cloud-controller-manager lets you integrate your cluster into an existing network or cloud of your provider. The cloud-controller-manager then manages the interaction with the external components.

[Cloud Controller Manager](https://kubernetes.io/docs/concepts/architecture/cloud-controller/)

### kube-apiserver

The kube-apiserver is the interface for the outside world to interact with kubernetes. This means you can create and read kubernets objects over the kube-apiserver. These kubernets objects include pods, services, controllers and much more. Concepts of the kubernetes api are documented [here](https://kubernetes.io/docs/reference/using-api/api-concepts/)

Since this is a crucial component, it is also specifically documented here: [[Kubernetes Object-API]]

[kube-apiserver cli](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-apiserver/)

### kube-scheduler

The kube-scheduler is responsible to run newly created pods on the cluster nodes by applying scheduling principles. These principles contain two operations. First it filters all possible nodes from the set of all nodes and then in a second step applies a scoring system which eventually decide on which node the new pod is run. You can scheduler can be configured using [scheduling policies](https://kubernetes.io/docs/reference/scheduling/policies/). The scheduling policies contain Predicates which are applied during the filter operation and Priorities which are applied during the scoring operation of the scheduler.

[kubernetes scheduler](https://kubernetes.io/docs/concepts/scheduling-eviction/kube-scheduler/)
[kube-scheduler cli](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-scheduler/)
#### etcd

etcd is a distributed key-value store for highly available systems.

[etcd docs](https://etcd.io/docs/)

## Node Components

A cluster node must have at least following components running:

- kubelet
- kube-proxy

The nodes sole purpose is to run pods within them and therefore are the working horses of kubernetes, steering the application workload.

### kubelet

The kubelet is like a shepherd and takes care of the pods running on the respective node. If a pod is not healty, kubelet resolves the issues if possible. Which metrics and techniques are applied by kubelet is defined in a so called PodSpec.

[kubelet cli](https://kubernetes.io/docs/reference/command-line-tools-reference/kubelet/)

### kube-proxy

The kube-proxy is a proxy running on each node of the cluster and handling incoming as well as outgoing traffic and applying as well as maintaining network rules.

[kube-proxy cli](https://kubernetes.io/docs/reference/command-line-tools-reference/kube-proxy/)

## The Container Runtime

Each node which shall be capable of running pods must run a container runtime which is conformant with the [Kubernetes Container Runtime Interface (CRI)](https://github.com/kubernetes/community/blob/master/contributors/devel/sig-node/container-runtime-interface.md)

---
links: [[000 Index|Index]], [[300 Kubernetes MOC]]