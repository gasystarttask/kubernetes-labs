**Lab 7:** Change Service type to NodePort and access via node IP.

Run:
```bash
kubectl patch service web -p '{"spec":{"type":"NodePort"}}'
kubectl get service web
```
### Service Type Comparison:
1. **ClusterIP** (default): Only accessible within the cluster
1. **NodePort**: Accessible from outside the cluster using <NodeIP>:<NodePort>
1. **LoadBalancer**: Creates an external load balancer (cloud provider specific)
1. **ExternalName**: Maps service to an external DNS name

👉 Goal: See that a Service is a stable access point for dynamic Pods.