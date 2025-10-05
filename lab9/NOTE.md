**Lab 9:** Use labels and list by selectors:

Run:
```bash
kubectl label pods nginx env=dev -n dev
kubectl get pods -l env=dev -n dev
```

👉 Goal: Develop comfort querying and organizing workloads via labels.