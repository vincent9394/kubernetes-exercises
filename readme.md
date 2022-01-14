This is the exercise of k8s, which mainly based on Kind 

# install Kind in WSL2
```
curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.11.1/kind-linux-amd64
chmod +x ./kind
sudo mv ./kind /usr/local/bin/
```

# install kind in macOS
```
brew install kind
```


# Basic kind command 
```
kind create cluster
kind create cluster --name <cluster-name> --image <kindest/node:v1.17.5>
kind get clusters
kind delete cluster
kind delete cluster --name <cluster-name>
```

# Basic kubectl command 
```
kubectl cluster-info --context kind-kind
kubectl get nodes
kubectl get pods
```







# Reference:
https://kind.sigs.k8s.io/docs/user/quick-start/
https://blog.miniasp.com/post/2020/08/21/Install-Kubernetes-cluster-in-WSL-2-Docker-on-Windows-using-kind

