# 3-Tier Web Application Deployed on Kubernetes

This project demonstrates a simple 3-tier web application deployed on a Kubernetes cluster. The application consists of the following components:

-   **Frontend:** nginx deployment configed to be a loadbalncer and web facing tier with NodePort service.
-   **Backend API:** wordpess deployment as backend with ClusterIP service.
-   **Database:** A MySQL database deployment storing application data with CluesterIP service.




## Prerequisites

Before we dive in, you'll need to have the following installed on your system:

-   **Virtualization software** VirtualBox, or Hyper-V.
-   **Sufficient system resources::** CPU, memory, and disk space
-   **Minikube:** Refer to the official Minikube documentation for detailed instructions based on your operating system: [https://kubernetes.io/docs/setup/minikube/](https://kubernetes.io/docs/setup/minikube/)
-   **Kubectl:** -   Download the appropriate kubectl binary for your operating system from the Kubernetes website: [https://kubernetes.io/docs/tasks/tools/install-kubectl/](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

![](https://github.com/eranmekler/3_tier_webapp_kubernetes/blob/main/3_tier_kubernetes.drawio.svg)

## Deployment on Kubernetes:

>The project utilizes Kubernetes manifests (YAML files) to define and deploy the application components as pods and services within the cluster.

### Key Features:

-   Multi-container application showcasing separation of concerns. **(microservices)**.
-   Containerization for portability and scalability.
-   Kubernetes deployment for automated deployment and management.

## Getting Started:

>Before deploying this application, ensure you have a functional Kubernetes cluster running.

**Clone the repository:**

`git clone https://github.com/eranmekler/3_tier_webapp_kubernetes.git`


**Deploy the application:**
   
 	`cd 3_tier_webapp_kubernetes`
 	`kubectl apply -f frontend/`
 	`kubectl apply -f backend/`
 	`kubectl apply -f db/`



## Access the application:

`minikube service nginx-service`
(will open the browser automatically)



# Further Considerations:

-   This is a basic example, and the deployment configuration can be customized for specific needs.
-   Security measures should be implemented before deploying the application in a production environment.
