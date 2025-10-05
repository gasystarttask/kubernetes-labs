**Lab 8:** Create tow Namespaces:

Run:
```bash
kubectl create ns dev
kubectl create ns prod
```
Deploy different apps:

```bash
kubectl run nginx --image=nginx -n dev
kubectl run nginx --image=nginx -n prod
```

