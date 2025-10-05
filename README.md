### ☸️ **Kubernetes Core Terminology**

#### **1. Cluster**

* The **entire Kubernetes environment** that runs and manages containerized applications.
* It consists of:

  * **Control Plane** → manages and orchestrates the system (API server, scheduler, controller manager, etcd).
  * **Worker Nodes** → actually run your application workloads (Pods).

🧠 *Think of a cluster as the “whole Kubernetes system” — the brain (control plane) and muscles (nodes) working together.*

---

#### **2. Node**

* A **machine** (physical or virtual) that runs part of your application.
* Each node runs:

  * `kubelet` (agent that talks to the control plane)
  * `kube-proxy` (network routing)
  * A container runtime (like containerd or CRI-O)

🧠 *A node is a worker where your containers actually live and run.*

---

#### **3. Pod**

* The **smallest deployable unit** in Kubernetes.
* A pod can hold **one or more tightly coupled containers** that share:

  * Network (same IP)
  * Storage volumes
  * Lifecycle

🧠 *A pod = a single instance of your app (or part of it). It’s what Kubernetes schedules onto nodes.*

---

#### **4. Deployment**

* A **controller** that manages pods for stateless applications.
* It:

  * Ensures the desired number of pods are always running (self-healing)
  * Handles rolling updates and rollbacks

🧠 *A deployment keeps your pods running the way you want — it’s the “manager” of replicas.*

---

#### **5. Service**

* A **stable network endpoint** that exposes a set of pods to other pods or external users.
* It automatically load-balances traffic between pods using labels and selectors.

🧠 *A service = a consistent “door” to reach your pods, even as pods die and restart.*

---

### 🔗 **Visual Summary**

```bash
[ Cluster ]
 ├── [ Control Plane ]
 └── [ Node(s) ]
       └── [ Pod(s) ]
             ├── Container(s)
             └── Managed by → [ Deployment ]
       └── Accessed via → [ Service ]
```

---
