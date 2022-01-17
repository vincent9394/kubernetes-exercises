## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## create role
```
kubectl apply -f role.yml

```

## Bind the role to the dev user
```
kubectl apply -f rolebinding.yml
```

## check the role
```
kubectl describe role pod-reader
```

## delete the role
```
kubectl delete role pod-reader
```

## Reference
https://www.bogotobogo.com/DevOps/Docker/Docker-Kubernetes-RBAC.php#:~:text=The%20RBAC%20mechanism%20enables%20us,specific%20namespace%20of%20our%20cluster.
