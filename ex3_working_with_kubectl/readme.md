## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## Create a pod by config yml
```
kubectl apply -f pod.yml 
```

## Experiment with various output formats.
```
kubectl get pods -o wide   
kubectl get pods -o json  
kubectl get pods -o yaml 
```

## Filter results by a label.
```
kubectl get pods -n kube-system --selector k8s-app=calico-node
```

## Describe a pod.
```
kubectl describe pod my-pod      
```

## Execute a command inside a pod
```
kubectl exec my-pod -c busybox -- echo "hello world"   
```

## Delete a  pod
```
kubectl delete pod my-pod     
```