**Lab 10:** Create and inject a ConfigMap:

Run:
```bash
kubectl create configmap app-config --from-literal=APP_MODE=dev

```

Reference it in Pod spec (YAML):

```yaml
env:
- name: APP_MODE
  valueFrom:
    configMapKeyRef:
      name: app-config
      key: APP_MODE
```

