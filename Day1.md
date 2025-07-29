## ✅ Day 1: Kubernetes Architecture & Core Components

<img width="6912" height="3456" alt="K8s Architecture" src="https://github.com/user-attachments/assets/b75355a9-f062-4445-8e7b-81aae42c9373" />


### 🚀 Control Plane (Master Node) Components

- **API Server**  
  The communication hub for the cluster. All requests (e.g., `kubectl`, UI) go through the API server, which validates and routes them.

- **Scheduler**  
  Assigns new pods to appropriate nodes based on resource availability, affinity rules, and constraints.

- **etcd**  
  A distributed key-value store that holds the cluster state — nodes, pod specs, config maps, secrets, etc.

- **Controller Manager**  
  Keeps the cluster's actual state aligned with its desired state. Manages ReplicaSets, endpoints, nodes, etc.

- **Cloud Controller Manager**  
  Handles cloud-specific integrations (like AWS, GCP). Manages load balancers, volumes, and cloud networking.

---

### 🧱 Worker Node Components

- **Kubelet**  
  Agent on each node. Talks to the API server and ensures containers run as expected.

- **Kube-proxy**  
  Handles networking rules, pod communication, and service exposure using iptables/IPVS.

- **Pods**  
  The smallest deployable unit. A pod can contain one or more containers sharing the same network and storage.

- **Container Runtime**  
  Responsible for running containers. Common runtimes include Docker, containerd, and CRI-O.

---

### 📦 Other Important Concepts

- **Namespace**  
  Used for logical isolation within the cluster. Helps manage resources across teams or environments.

- **Deployment**  
  Ensures the desired number of pods are running, and manages updates and rollbacks.

- **Service**  
  Provides stable access to a set of pods. Types include `ClusterIP`, `NodePort`, and `LoadBalancer`.

- **Ingress**  
  Manages external HTTP/S traffic into the cluster with path or host-based routing.

- **Volume**  
  Enables persistent storage for pods, useful beyond the lifecycle of a single pod.

- **RBAC (Role-Based Access Control)**  
  Defines who can access what in the cluster. Applies to users, groups, and service accounts.

---

### 📝 Quick Reference Table

| Component              | Purpose                                                  |
|------------------------|----------------------------------------------------------|
| **API Server**         | Handles all communication with the cluster               |
| **etcd**               | Stores cluster data (nodes, pods, configs, etc.)         |
| **Scheduler**          | Decides which node a pod will run on                     |
| **Controller Manager** | Ensures actual state matches desired state               |
| **Cloud Ctrl Manager** | Manages cloud integrations (LBs, volumes, etc.)          |
| **Kubelet**            | Manages containers on nodes                              |
| **Kube-proxy**         | Manages networking rules and routing                     |
| **Pod**                | Basic unit that runs containers                          |
| **Container Runtime**  | Runs containers (Docker, containerd, CRI-O)              |
| **Namespace**          | Logical resource separation                              |
| **Deployment**         | Manages replicas and updates of pods                     |
| **Service**            | Exposes pods for internal/external communication         |
| **Ingress**            | Handles HTTP routing from outside the cluster            |
| **Volume**             | Provides persistent storage to pods                      |
| **RBAC**               | Access control for cluster resources                     |

---

- stay tuned for the next day challenge
