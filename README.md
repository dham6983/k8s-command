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
kubectl get deplo

```
