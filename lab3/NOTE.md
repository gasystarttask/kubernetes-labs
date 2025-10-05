**Lab 3:** Create a Pod using a YAML manifest:
```yml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx
    image: nginx
    ports:
    - containerPort: 80

```
Run:
```bash
kubectl apply -f nginx.yaml
kubectl logs nginx-pod
```

👉 Goal: Understand that Pods are ephemeral; when they die, they don’t auto-restart without higher-level controllers.