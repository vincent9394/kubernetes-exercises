## Create cluster with the config.yml
```
kind create cluster --config=config.yml

kubectl apply -f pod.yml

kubectl apply -f deployment.yml
```

# check the pod
```
kubectl get pods -o wide
```
(Find the deployment node and the pod node)

# Drain the node
```
kubectl drain <node name> --ignore-daemonsets --force
kubectl drain vincent-cluster-worker2 --ignore-daemonsets --force
```
# check the pod again
```
kubectl get pods -o wide
```
(the node should be changed)

# uncordon the node
```
kubectl uncordon <node name>
kubectl uncordon vincent-cluster-worker3
```