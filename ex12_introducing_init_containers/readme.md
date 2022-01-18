## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## Create pod
```
kubectl create -f init-pod.yml
```

## check the pod, You should see it remain in an Init state until the 30-second delay passes, then it should fully start up.
```
kubectl get pod init-pod
```