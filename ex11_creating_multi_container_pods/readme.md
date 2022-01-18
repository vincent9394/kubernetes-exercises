## Create Pod
```
kubectl create -f multi-container-pod.yml
kubectl create -f sidecar-pod.yml
```

## get pod
```
kubectl get pod multi-container-pod
kubectl get pod sidecar-pod
```

## Views the log
```
kubectl logs sidecar-pod -c sidecar
```