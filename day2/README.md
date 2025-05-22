## Resource Requests and Limits

- CPU Request: 250m (which means 0.25 CPU cores)
- CPU Limit: 500m (0.5 CPU cores)
- Memory Request: 64Mi (64 mebibytes)
- Memory Limit: 128Mi

## Why set CPU/memory requests and limits?

In a production environment, setting **resource requests and limits** ensures that each container has the necessary CPU and memory resources to run reliably without impacting other workloads on the cluster. 

- **Requests** reserve resources so the scheduler can place the pod on a node that can meet these minimum needs.
- **Limits** cap the maximum resources a container can use, preventing any single pod from exhausting node resources, which could degrade the performance or availability of other applications.

This resource management leads to better **stability**, **predictability**, and **fair resource distribution** across multiple applications in a shared cluster.

---
## When is node affinity used?
Node affinity is applied when there is a need to schedule pods on specific nodes based on labels or characteristics. Typical scenarios include:

- Deploying workloads that require **special hardware** (e.g., GPU nodes).
- Ensuring pods run in a particular **availability zone** or **data center** for latency or compliance reasons.
- Isolating critical workloads on dedicated nodes to avoid noisy neighbors.
- Optimizing resource usage or managing **node-specific constraints**.

By using node affinity, product teams gain greater **control over pod placement**, improving performance, compliance, or infrastructure utilization.

---
## Affinity Rule Used
In `node-affinity.yaml`, we used:
```yaml
  nodeAffinity:
    requiredDuringSchedulingIgnoredDuringExecution:
      nodeSelectorTerms:
      - matchExpressions:
        - key: kubernetes.io/hostname
          operator: In
          values:
          - docker-desktop