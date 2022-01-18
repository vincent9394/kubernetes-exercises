## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## Create pod
```
kubectl create -f always-pod.yml
kubectl create -f never-pod.yml
kubectl create -f onfailure-pod.yml
```

## get pod
```
kubectl get pod always-pod
kubectl get pod never-pod
kubectl get pod onfailure-pod
```