# Kubernetes Syllabus

**Week 1: Introduction to Kubernetes & Containerization**

*   What is Kubernetes? Why use it?
*   Containerization Fundamentals: Docker basics (images, containers, Dockerfile)
*   Kubernetes Architecture: Master Node, Worker Nodes, etcd, API Server, Scheduler, Controller Manager, Kubelet, Kube-proxy
*   Setting up a Local Kubernetes Environment: Minikube/Kind/Docker Desktop

**Week 2: Kubernetes Core Concepts: Pods & Deployments**

*   Pods: Definition, Lifecycle, Multi-container Pods
*   Deployments: Declarative Updates, Rollouts, Rollbacks
*   ReplicaSets: Scaling and Maintaining Pod Replicas
*   YAML Manifests: Structure, Best Practices

**Week 3: Services and Networking**

*   Services: Exposing Applications, Service Types (ClusterIP, NodePort, LoadBalancer)
*   Networking in Kubernetes: DNS, Internal/External Communication
*   Ingress Controllers: Exposing Services with Ingress Resources
*   Network Policies: Controlling Network Traffic

**Week 4: Configuration & Secrets Management**

*   ConfigMaps: Externalizing Configuration Data
*   Secrets: Managing Sensitive Information
*   Environment Variables: Injecting Configuration into Containers
*   Best Practices for Configuration Management

**Week 5: Storage & Persistence**

*   Volumes: Persistent vs. Ephemeral Storage
*   Persistent Volumes (PVs) & Persistent Volume Claims (PVCs)
*   Storage Classes: Dynamic Provisioning
*   Understanding different storage options (e.g., cloud providers, NFS)

**Week 6: Health Checks & Monitoring**

*   Liveness Probes: Restarting Unhealthy Containers
*   Readiness Probes: Preventing Traffic to Unready Containers
*   Startup Probes: Handling Slow-Starting Applications
*   Monitoring with Prometheus & Grafana (Introduction)

**Week 7: Namespaces & Resource Management**

*   Namespaces: Organizing Resources, Multi-tenancy
*   Resource Quotas: Limiting Resource Consumption
*   Limits & Requests: CPU and Memory Management
*   Best Practices for Resource Allocation

**Week 8: Security & Access Control**

*   Role-Based Access Control (RBAC): Users, Groups, Roles, RoleBindings
*   Service Accounts: Identity for Pods
*   Network Policies (revisited): Further Security Enforcement
*   Security Contexts: Fine-grained Security Controls

**Week 9: Advanced Kubernetes Concepts**

*   DaemonSets: Ensuring a Pod Runs on Each Node
*   Jobs & CronJobs: Running Batch Tasks
*   StatefulSets: Managing Stateful Applications (e.g., Databases)
*   Operators (Introduction): Automating Complex Deployments

**Week 10: Package Management with Helm**

*   Helm: Package Manager for Kubernetes
*   Helm Charts: Structure, Templates, Values
*   Installing and Managing Applications with Helm
*   Creating Custom Helm Charts

**Week 11: Kubernetes on Cloud Providers (AWS, GCP, Azure - Introduction)**

*   Managed Kubernetes Services: EKS, GKE, AKS
*   Provisioning and Configuring Clusters on Cloud Providers
*   Cloud Provider Integrations: Load Balancers, Storage
*   Cost Optimization Strategies

**Week 12: CI/CD with Kubernetes**

*   Integrating Kubernetes into CI/CD Pipelines
*   Automated Deployment Strategies (Blue/Green, Canary)
*   Tools for CI/CD (e.g., Jenkins, GitLab CI, Argo CD)
*   Best Practices for Continuous Delivery

**Week 13: Troubleshooting & Debugging**

*   Debugging Kubernetes Applications
*   Analyzing Logs: Centralized Logging Solutions
*   Monitoring and Alerting: Identifying Issues Early
*   Common Kubernetes Errors and Solutions

**Week 14: Future of Kubernetes & Emerging Technologies**

*   Serverless Computing (Knative)
*   Service Mesh (Istio, Linkerd)
*   Edge Computing with Kubernetes
*   Kubernetes Community & Ecosystem
