# Flux-Home

Welcome to the **flux-home** repository! This repository contains the Kubernetes manifests for my K3s Kubernetes cluster at home. It enables me to manage my cluster efficiently and automate the deployment of applications using various tools and services.

## 🔧 Tools Used

- [Cert Manager](https://cert-manager.io/): Cert Manager is a Kubernetes add-on that automates the management and provisioning of TLS certificates. It simplifies the process of obtaining and renewing certificates from certificate authorities like Let's Encrypt. It uses Cloudflare DNS to generate Let's Encrypt certificates, ensuring secure communication for both external and internal-only services.

- [External DNS](https://github.com/kubernetes-sigs/external-dns): External DNS is a Kubernetes add-on that automatically manages DNS records for your services and ingresses. It integrates with various DNS providers, ensuring that DNS entries are updated dynamically as your services and ingresses change. I have configured two instances of External DNS:

  1. External DNS (Cloudflare): Manages my external Cloudflare DNS records, allowing external access to my services.

  2. Internal DNS (Active Directory via RF2136): Manages my internal Active Directory DNS records using RFC 2136 dynamic DNS updates. This enables internal access to services within my cluster.

- [FluxCD](https://fluxcd.io/): FluxCD is a GitOps operator that helps in automating the deployment and lifecycle management of Kubernetes applications. It synchronizes the cluster state with the Git repository, ensuring that the desired state is always maintained.

- [GarageHQ](https://garagehq.deuxfleurs.fr/): GarageHQ is a lightweight, self-hosted object storage system compatible with the Amazon S3 API. It allows you to store and retrieve data using the S3 protocol within your Kubernetes cluster.

- [Ingress-Nginx](https://github.com/kubernetes/ingress-nginx): Ingress-Nginx is an Ingress controller for Kubernetes that enables the routing of incoming traffic to your services. It provides features like SSL/TLS termination, load balancing, and path-based routing.

- [OnePassword Connect + Operator](https://github.com/1Password/onepassword-operator): The OnePassword Operator is a tool for integrating the 1Password secrets management platform with Kubernetes. It provides secure and convenient access to secrets and credentials for your applications. The Operator uses OnePassword Connect to fetch the secrets from 1Password.

- [Rancher Longhorn](https://longhorn.io/): Longhorn provides a distributed block storage system for Kubernetes, offering replicated storage with high availability and data durability.

- [Renovate](https://www.mend.io/renovate/): Renovate is an automated dependency management tool. It keeps track of the dependencies in your project and automatically updates them to their latest versions, ensuring that your cluster stays up-to-date and secure.

- [Tekton](https://tekton.dev/): Tekton is a flexible and scalable Kubernetes-native framework for building Continuous Integration/Continuous Delivery (CI/CD) systems. It allows you to define and run CI/CD pipelines as code, enabling automation and collaboration.

## 💻 Kubernetes Nodes

| Name   | Node                | Processor           | Memory   | Storage |
|--------|---------------------|---------------------|----------|---------|
| Ananke | Prodesk 400 G5      | Intel Core i5-9500T | 16 GB    | 1TB SSD |
| Nyx    | Prodesk 400 G3      | Intel Core i5-7500T | 8 GB     | 1TB SSD |
| Ourea  | Prodesk 800 G2 (VM) | Intel Core i5-6500T | 8 GB     | 1TB SSD |

These nodes collectively form the backbone of my home Kubernetes cluster, providing the necessary resources for running and managing containerized applications.

## 🤖 AI-Generated Disclaimer

Disclaimer: This README was generated with the assistance of artificial intelligence (AI). While efforts have been made to ensure the accuracy and clarity of the information presented, please note that the content may not always reflect human-written documentation.
If any of the links are incorrect, I might have missed checking them.
Use the provided information at your own discretion and if in doubt refer to official documentation.
