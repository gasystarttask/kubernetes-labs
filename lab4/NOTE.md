**Lab 4:** Create a Deployment:

Run:
```bash
kubectl create deployment web --image=nginx --replicas=3
```

Scale and rollout:
```bash
kubectl scale deployment web --replicas=5
kubectl rollout history deployment/web
```