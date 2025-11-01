# 🌍 3-Tier Cloud Application on Azure Kubernetes Service (AKS)

This project demonstrates a **three-tier cloud application** deployed on **Azure Kubernetes Service (AKS)**, showcasing containerization, orchestration, and monitoring in a modern DevOps workflow.  
It integrates **React**, **Node.js**, **MongoDB**, and **Redis** into a single scalable environment managed entirely with **Kubernetes**.

---

## 🏗️ Project Overview

The project was designed to highlight the use of **Kubernetes** as a scalable orchestration platform for a full-stack web application.  
It combines containerized frontend and backend components with managed databases, enabling seamless deployment, scaling, and monitoring on Azure.

<img width="1261" height="709" alt="image" src="https://github.com/user-attachments/assets/7b95c3b5-429c-44ca-9587-d393268e6d26" />
<img width="1261" height="709" alt="image" src="https://github.com/user-attachments/assets/11cb007e-8202-4f73-8eab-afd4be587717" />
<img width="1261" height="709" alt="image" src="https://github.com/user-attachments/assets/6a2884ac-e560-405d-b8dc-ff6f04daf011" />


---

## 💡 Application Architecture

A complete **3-tier architecture** consisting of:

1. **Frontend:** Built with **React** and **Vite** for a responsive user interface.  
2. **Backend:** Developed using **Node.js** and **Express** to handle business logic and APIs.  
3. **Databases:**  
   - **MongoDB** for primary data storage.  
   - **Redis** for caching and session management.

---

## 🐳 Containers

To containerize the stack:

- Created individual **Dockerfiles** for the frontend and backend services.  
- Used **Docker Compose** to run and test containers locally.  
- Verified smooth communication between all services before deployment.  

---

## 📦 Push to Azure Container Registry (ACR)

Once the containers were verified locally, they were built and pushed to **Azure Container Registry (ACR)**.

Steps:
1. Built Docker images for both **frontend** and **backend**.  
2. Tagged and pushed them to ACR using custom image names.  
3. Verified successful uploads before deployment to AKS.  

---

## ☸️ Kubernetes (AKS)

After pushing the images to ACR, the next step was deploying them to **Azure Kubernetes Service (AKS)** to achieve orchestration and scalability.

---

## 🧩 Deployment Process

### 1️⃣ Cluster Setup
- Created an **AKS Cluster** on Azure.  
- Linked the cluster with **Azure Container Registry (ACR)** to automatically pull container images.

---

### 2️⃣ YAML Configuration
Prepared and applied Kubernetes manifests for **Deployments** and **Services**.

| Component | Purpose |
|------------|----------|
| `frontend` | Runs the React/Vite web interface |
| `backend`  | Hosts the Node.js + Express API layer |
| `mongo`    | Stores persistent application data |
| `redis`    | Handles caching and session management |

---

### 3️⃣ Deployment Execution
- Applied manifests using `kubectl apply -f`.  
- Verified pod creation and internal communication.  
- Ensured all components were running as **Pods** inside the AKS cluster, forming the complete 3-tier architecture.  

---

## 🌐 Ingress Configuration

To route and manage external traffic efficiently:

1. Installed **Ingress Controller** within the AKS cluster.  
2. Configured **Ingress rules** to route requests between frontend and backend services.  
3. Verified accessibility through the public endpoint.  

---

## 📊 Monitoring & Observability

To ensure visibility and track performance:

- Installed **Prometheus** to collect metrics from pods.  
- Deployed **Grafana** for real-time dashboards.  
- Connected Grafana to Prometheus as the primary data source.  

This provided insights into resource usage, pod health, and application performance.

---

## 🧰 Tools & Technologies

| Layer | Tools |
|--------|--------|
| Frontend | React, Vite |
| Backend | Node.js, Express |
| Databases | MongoDB, Redis |
| Containerization | Docker, Docker Compose |
| Orchestration | Kubernetes (AKS) |
| Registry | Azure Container Registry (ACR) |
| Networking | Ingress Controller |
| Monitoring | Prometheus, Grafana |

---

## 🌟 Key Highlights

✔️ Built and deployed a complete **3-tier web application** on AKS.  
✔️ Implemented full containerization using **Docker** and **ACR**.  
✔️ Automated service routing with **Kubernetes Ingress**.  
✔️ Integrated **Prometheus** and **Grafana** for monitoring.  
✔️ Validated microservice communication both locally and in the cluster.  

---

## 🔗 Related Repositories

- [ First Project](https://github.com/ibrahim3321/the-last-projects-.git)  
- [Second Project](https://github.com/anas-443005129/master_projectg6.git)  

---

## 🏁 Conclusion

This project successfully demonstrates a **cloud-native 3-tier application** running on **Azure Kubernetes Service (AKS)**.  
It combines containerization, orchestration, and monitoring to achieve a modern DevOps workflow capable of scaling efficiently and maintaining visibility across all application components.

---
