## create the config map
```
kubectl create -f my-configmap.yml     
```

## see the configmap data
```
kubectl describe configmap my-configmap
```

```
echo -n 'secret' | base64   

// c2VjcmV0


echo -n 'anothersecret' | base64

// YW5vdGhlcnNlY3JldA==
```

## generate the my-secret with the hashed secret
```
kubectl create -f my-secret.yml
```

## get the secret
```
kubectl get secret
```


## Create the end-pod
```
kubectl create -f env-pod.yml
```

## check the log of end-pd
```
kubectl logs env-pod
// you will see:" configmap: Hello, world! secret: secret "
```

## Create the volume-pod
```
kubectl create -f volume-pod.yml
```

## Use kubectl exec to see the file
```
kubectl exec volume-pod -- ls /etc/config/configmap   
// key1
// key2

kubectl exec volume-pod -- cat /etc/config/configmap/key1  
// Hello, world!

kubectl exec volume-pod -- cat /etc/config/configmap/key2
// Test
// multiple lines
// more lines

kubectl exec volume-pod -- ls /etc/config/secret
// secretkey1
// secretkey2

kubectl exec volume-pod -- cat /etc/config/secret/secretkey1
// secret

kubectl exec volume-pod -- cat /etc/config/secret/secretkey2
// anothersecret

```