## Create cluster with the config.yml
kind create cluster --config=config.yml

## Kube create deployment
## Kube save the yaml file
```
kubectl create deployment my-deployment04-1 --image=nginx --dry-run -o yaml > deploy04-1.yml

```

## //IMPORTANT 
```
name cannot not contain "_"

The Deployment "my-deployment04_1" is invalid: metadata.name: Invalid value: "my-deployment04_1": a lowercase RFC 1123 subdomain must consist of lower case alphanumeric characters, '-' or '.', and must start and end with an alphanumeric character (e.g. 'example.com', regex used for validation is '[a-z0-9]([-a-z0-9]*[a-z0-9])?(\.[a-z0-9]([-a-z0-9]*[a-z0-9])?)*')
```

## Create the object using the file.
```
kubectl create -f deploy04-1.yml  
```
## Get the deployment.
```
kubectl get deployment
```

## Scale a deployment and record the command.
```
kubectl scale deployment my-deployment04-1 --replicas=5 
```

## see the replicas
```
kubectl describe deployment my-deployment04-1
```
