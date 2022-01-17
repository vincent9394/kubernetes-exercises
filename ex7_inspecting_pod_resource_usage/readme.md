
## apply from the web
```
kubectl apply -f https://raw.githubusercontent.com/linuxacademy/content-cka-resources/master/metrics-server-components.yaml
```

## Check the results
```
kubectl get --raw /apis/metrics.k8s.io
```
```
//Result
{"kind":"APIGroup","apiVersion":"v1","name":"metrics.k8s.io","versions":[{"groupVersion":"metrics.k8s.io/v1beta1","version":"v1beta1"}],"preferredVersion":{"groupVersion":"metrics.k8s.io/v1beta1","version":"v1beta1"}}
```
## see the pods
```
kubectl get pods -n kube-system  
```

## create the pod
```
kubectl apply -f pod.yml
```


## Top pod to see the resources
```
kubectl top pod
```

## if error occur
```
W1122 10:41:57.632230   38445 top_pod.go:140] Using json format to get metrics. Next release will switch to protocol-buffers, switch early by passing --use-protocol-buffers flag
Error from server (ServiceUnavailable): the server is currently unable to handle the request (get pods.metrics.k8s.io)
```



## Type the follow command
```
kubectl edit deploy metrics-server -n kube-system

// delete the amd64
```

## Sort top  by --sort-by
```
kubectl top pod --sort-by cpu
```

## Filter output by label with --selector 
```
kubectl top pod --selector app-metrics-test
```