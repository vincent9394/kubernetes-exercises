## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## Create a pod with resource requests that exceed aviable node resources.
```
kubectl create -f big-request-pod.yml
```
## Check the pod status. It should never leave the Pending state since no worker nodes have enough resources to meet the request.
```
kubectl get pod big-request-pod    
```

## Create a pod with resource requests and limits.
```
kubectl create -f resource-pod.yml   
```

## Check the pod status.
```
kubectl get pod resource-pod  
```

## Check the pod status.
```
kubectl get pods
```