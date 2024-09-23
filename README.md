# Kubernetes Gateway API with Service Mesh: Traffic Management Demo

## Project Overview

This repository demonstrates an advanced traffic management scenario in Kubernetes using the **Gateway API** along with a **Service Mesh** (Istio) for managing both **north-south** (external-to-internal) and **east-west** (internal service-to-service) traffic. The example highlights the collaboration of three different roles—**Infrastructure Provider**, **Cluster Operator**, and **Application Developer**—to showcase the flexibility and extensibility of the **Gateway API**.

### Key Features

- Manage **north-south** traffic through a **single Gateway**.
- Secure and manage **east-west** traffic using a **Service Mesh** (Istio).
- Demonstrate how different roles interact in real-world Kubernetes environments:
  - **Infrastructure Provider**: Sets up networking infrastructure, including the GatewayClass and Gateway.
  - **Cluster Operator**: Configures traffic routing and ensures Istio integration for the Service Mesh.
  - **Application Developer**: Deploys applications and defines traffic routing rules.

---

## Project Structure

```bash
k8s-gateway-api-service-mesh-demo/
├── README.md
├── infrastructure/
│   ├── cluster
│       ├── kind-config.yaml
│   ├── gatewayclass.yaml
│   ├── gateway.yaml
│   └── install-istio.sh
├── apps/
│   ├── frontend/
│   │   ├── frontend-deployment.yaml
│   │   ├── httproute-frontend.yaml
│   └── backend/
│       ├── backend-deployment.yaml
│       ├── httproute-backend.yaml
├── policies/
│   └── peer-authentication.yaml
└── docs/
    └── roles-and-personas.md
