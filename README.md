# 🚀 Kubernetes Web Stack Deployment

This repository contains the necessary configuration files and scripts to deploy a structured, multi-service web application stack using **Kind (Kubernetes in Docker)** for local development and testing.

The stack utilizes **NGINX** and **Apache2** as front-end services, backed by a persistent **MySQL** database.

## 📁 Repository Structure

The project is organized into the following key components:

| File/Directory | Description |
| :--- | :--- |
| `apache2/` | Kubernetes manifests and configuration files for deploying the **Apache HTTP Server** (e.g., Deployments, Services, ConfigMaps). Apache is often used for serving dynamic content or a backend application server. |
| `config.yml` | A centralized configuration file (likely a Kubernetes ConfigMap or application configuration) defining environment variables and settings for the deployed services. |
| `kind.sh` | A comprehensive shell script for managing the Kind cluster lifecycle (e.g., `create-cluster`, `delete-cluster`, `load-images`). **Always review this script before execution.** |
| `mysql/` | Kubernetes manifests for the **MySQL** database, including PersistentVolumeClaims (PVC) for data persistence, Deployments, and necessary Secrets. |
| `nginx/` | Kubernetes manifests and configuration files for the **NGINX** web server. NGINX typically acts as an Ingress Controller or a high-performance reverse proxy in this setup. |
| `README.md` | This documentation file. |

---

## 🛠️ Prerequisites

To run this stack successfully, please ensure you have the following tools installed and configured:

* **Docker:** Required as Kind uses Docker containers to run Kubernetes nodes.
* **kubectl:** The Kubernetes command-line tool.
* **Kind (Kubernetes in Docker):** For creating and managing the local cluster.
* **Git:** For cloning the repository.

---

## 💻 Getting Started

### 1. Clone the Repository

Clone the project using the SSH URL you just configured:

```bash
git clone git@github.com:sayamuddinshams/k8s.git
cd k8s
