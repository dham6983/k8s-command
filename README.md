[Spinnaker training repo](https://github.com/redashu/salesforce-spinnaker-1)


## k8s-command

### Createing deployemnt yaml using CLI
```
kubectl  create  deployment debdemoapp  --image=dockerashu/jecrcapp:v1  --port 80 --dry-run=client -o yaml >app.yml

```

### deploy the manifest file 

```
kubectl apply -f app.yml

```

### verify the deployment

```
kubectl get deploy

```

### descibe the deployment

```
kubectl describe deploy debdemoapp

```

### Create the srvice manifest yaml


```
kubectl  expose deployment  debdemoapp  --type NodePort --port 80 --dry-run=client -o yaml >expose.yaml

```

### deploye the service manifest file

```
kubectl apply -f expose.yaml

```
### Verify the service

```
kubectl get services

```

### delete a sevice object

```
kubectl delete services debdemoapp

```

### delete all deployment object

```

kubectl delete deployment debdemoapp

```

### Create a namespace

```
kubectl create ns spinnaker

```

### Setting context to my namespace created above

```
kubectl config set-context --current --namespace spinnaker

```

### Getting a current context

```
kubectl config current-context

```
