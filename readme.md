
# Kubernetes Homelab (K3s)

This repo documents my **K3s-based Kubernetes homelab**, inspired by **Mischa van den Burg** and other DevOps experts. The goal is to build a lightweight, fully automated Kubernetes cluster using **GitOps, monitoring, and best practices**.

## 🛠️ Tech Stack
- **K3s** – Lightweight Kubernetes for homelabs
- **FluxCD** – GitOps for continuous deployments
- **Helm** – Managing Kubernetes apps
- **Prometheus & Grafana** – Monitoring and observability
- **Loki & Promtail** – Centralized logging
- **Longhorn** – Distributed storage
- **NGINX Ingress Controller** – Routing external traffic
- **Cert-Manager** – Automating SSL/TLS certificates
- **Metallb** – LoadBalancer for bare-metal
- **K9s** – Terminal-based Kubernetes UI

## 📌 Goals
✅ Lightweight & reproducible setup
✅ Automated deployments with GitOps
✅ Full observability (logs, metrics, dashboards)
✅ Secure & scalable architecture
✅ Self-hosted apps (future-proofing for SaaS)

## 📂 Repo Structure
```
.
├── manifests/        # Kubernetes YAML manifests
├── helm/            # Helm charts & values
├── flux/            # GitOps configs
├── monitoring/      # Prometheus, Grafana, Loki setup
├── scripts/         # Automation & helper scripts
└── README.md        # This file
```

## 🚀 Getting Started
### 1️⃣ Install K3s
```bash
curl -sfL https://get.k3s.io | sh -
```

### 2️⃣ Clone the Repo
```bash
git clone https://github.com/yourusername/k3s-homelab.git
cd k3s-homelab
```

### 3️⃣ Deploy FluxCD (GitOps)
```bash
kubectl apply -f flux/install.yaml
```

### 4️⃣ Deploy Monitoring Stack
```bash
helm install monitoring ./helm/monitoring -n monitoring --create-namespace
```

### 5️⃣ Verify the Cluster
```bash
kubectl get nodes
kubectl get pods -A
```

## 🔥 Roadmap
- [ ] Automate storage setup with Longhorn
- [ ] Deploy a self-hosted CI/CD pipeline
- [ ] Implement security best practices (RBAC, PodSecurityPolicies)
- [ ] Expand with additional self-hosted services

## 📝 Notes
This repo is **a work in progress**. Expect continuous improvements, refactoring, and optimizations.

If you're building your own homelab, feel free to fork this and adapt it to your needs. PRs and feedback are welcome! 🚀


