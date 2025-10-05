**Lab 6:** Expose your Deployment:

Run:
```bash
kubectl expose deployment web --port=80 --type=ClusterIP
```
Test with:

Option 1: Use a timeout parameter (Recommended)
```bash
kubectl run test --rm -it --image=busybox --timeout=60s -- nslookup web
```
Option 2: Create the pod first, then exec into it
```bash
# Create the pod
kubectl run test --image=busybox --restart=Never --command -- sleep 60

# Execute the nslookup command
kubectl exec test -- nslookup web

# Clean up
kubectl delete pod test
```
Option 3: Use a different approach to test connectivity
```bash
kubectl run test --rm -it --image=busybox --restart=Never -- sh -c "nslookup web && wget -qO- http://web"
```