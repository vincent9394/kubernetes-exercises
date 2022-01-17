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