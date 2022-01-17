## Create cluster with the config.yml
```
kind create cluster --config=config.yml
```

## Create a basic ServiceAccount
```
kubectl create -f my-serviceaccount.yml 

```

## Get the ServiceAccount
```
kubectl get serviceaccount
```

## Create a ServiceAccount with an imperative command.
```
kubectl create sa my-serviceaccount2 -n default
```

## Attach a Role to the ServiceAccount with a RoleBinding.
```
kubectl create -f sa-pod-reader.yml  
```

## delete the Service Account 
```
kubectl delete serviceaccount my-serviceaccount
kubectl delete sa my-serviceaccount2
```

## short form
```
kubectl get sa //serviceaccount
kubectl get po //pods
kubectl get ns  //namesapce
kubectl get no //node
```