**Lab 4:** Deploy an updated image and rollback:

Run:
```bash
kubectl set image deployment/web nginx=nginx:1.25
kubectl rollout undo deployment/web
```
👉 Goal: Master how Kubernetes achieves declarative self-healing through reconciliation loops.