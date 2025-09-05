# ArgoCD-Ops

A repository for managing Kubernetes application deployments and operations using ArgoCD and Helm. This project provides a Helm chart for a full-stack application and is intended for GitOps workflows and automated, declarative Kubernetes operations.

## Features

- **ArgoCD Ready**: Designed for seamless integration with ArgoCD for GitOps-driven deployments.
- **Helm Chart**: Contains a Helm chart (`k8s-fullstack-chart/`) for packaging, deploying, and managing a full-stack Kubernetes application.
- **Declarative Ops**: Keeps Kubernetes resources and configurations versioned and under source control.
- **Modular Structure**: Easily extend or customize for other applications or Kubernetes clusters.

## Repository Structure

- `k8s-fullstack-chart/` - Main Helm chart for deploying the full-stack application.
- `README.md` - Project overview and instructions.

## Getting Started

### Prerequisites

- [Helm](https://helm.sh/)
- [ArgoCD](https://argo-cd.readthedocs.io/en/stable/)
- Access to a Kubernetes cluster

### Usage

#### 1. Clone the repository

```bash
git clone https://github.com/doomerdpk-1802/ArgoCD-Ops.git
cd ArgoCD-Ops
```

#### 2. Install the Helm chart manually

```bash
helm install k8s-fullstack ./k8s-fullstack-chart
```
- Customize deployment by editing `values.yaml` inside the chart.

#### 3. Deploy with ArgoCD

- Create an ArgoCD Application resource pointing to this repository and the `k8s-fullstack-chart` path.
- ArgoCD will automatically manage syncing and rollout of the chart to your Kubernetes cluster.

