# k3d

## What is k3d ?

k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.

k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.

# Commands



``` bash
k3d cluster create my-cluster

```
* Creates a kubernetes cluster inside a container.
* Spin Up a Server Node
* Set up a Load Balancer
* Configure Your kubeconfig

### Check what you created :

``` bash
docker ps
```

``` bash 
kubectl get nodes
```

``` bash
kubectl get pods -n kube-system
```

``` bash
k3d cluster list
```

### Stop the clsuter without deleting it

the command kubectl won't work
``` bash
k3d cluster stop 'cluster-name'
```

##


``` bash
k3d cluster start 'cluster-name'
```

##


``` bash
k3d cluster delete 'cluster-name'
```

## 

``` bash  
kubectl create namespace namespace-name 
```

### Apply a configuration to a namespace

``` bash  
kubectl apply -n namespace-name -f file.yml 
```


### Port forward 
``` bash
kubectl port-forward svc/service_name -n namespace hostport:serviceport
```
