# 🚀 Kubernetes Custom Resource Definition (CRD) for CI/CD Automation Platform

🔧 **Extend Kubernetes like never before!**  
This repository demonstrates how to create a powerful **Custom Resource Definition (CRD)** to automate application CI/CD pipelines in Kubernetes, transforming your DevOps workflow.

## 🌟 Key Features

- **Custom CI/CD Pipeline**: Define and automate your entire application build and deployment process using a custom Kubernetes resource.
- **Multi-Platform Support**: Build and deploy applications across **Linux** and **Windows** environments.
- **Flexible Scaling**: Automatically scale your applications with predefined **T-shirt sizing** (small, medium, large) for CPU and memory.
- **Language Support**: Easily integrate applications written in **Python**, **C#**, **Go**, and more.
- **Environment-Specific Deployments**: Configure dev, test, and production environments seamlessly.

## 📑 Table of Contents

- [Overview](#overview)
- [Why Use This CRD?](#why-use-this-crd)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [CRD Example](#crd-example)
- [Contributing](#contributing)
- [License](#license)

---

## 🛠️ Overview

In the fast-paced DevOps world, managing and scaling application deployments efficiently is key. This **Kubernetes Custom Resource Definition (CRD)** adds a new dimension to Kubernetes, allowing you to define, build, and deploy applications with just a few simple commands. Perfect for creating your own **CI/CD platform** within Kubernetes, this resource is designed to simplify deployment processes while offering flexibility and scalability.

## ⚙️ Why Use This CRD?

This CRD offers a **dev-friendly** approach to continuous integration and deployment, making it easier for your team to:
- 🚀 **Automate complex CI/CD workflows** within Kubernetes clusters.
- 📈 **Improve efficiency** by reducing manual intervention for deployments.
- 🔄 **Scale with ease** based on traffic and resource needs.
- 💼 **Maintain consistent environments** across dev, test, and production.

Whether you're a seasoned DevOps engineer or just starting, this project empowers you to manage application lifecycles more effectively!

---

## 📂 Project Structure

```
.
├── crds/                     # CRD YAML definition files
├── examples/                 # Example CRD resource files
├── README.md                 # Project documentation (this file)
└── LICENSE                   # Licensing information
```

- **crds/**: Contains the YAML file for defining the Custom Resource Definition.
- **examples/**: Provides example Kubernetes manifest files that show how to use the custom resource in real-world scenarios.

---

## ⚡ Prerequisites

Before getting started, ensure you have the following:

- **Kubernetes Cluster**: A running Kubernetes cluster (Minikube, EKS, AKS, or GKE).
- **kubectl**: Installed and configured to interact with your Kubernetes cluster.
- **Docker**: Installed if you plan to build and push container images.

---

## 🚀 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/vishalgunjalSWE/K8s-Custome-Resource-Definition.git
   cd K8s-Custome-Resource-Definition
   ```

2. **Apply the CRD** to your cluster:
   ```bash
   kubectl apply -f crds/custom-resource-definition.yaml
   ```

3. **Verify** that the CRD has been installed successfully:
   ```bash
   kubectl get crds
   ```

4. **Deploy an example custom resource**:
   ```bash
   kubectl apply -f examples/custom-resource-example.yaml
   ```

---

## 📝 Usage

### Custom Resource Attributes

- **appId**: A unique string identifier for your application.
- **codeLanguage**: Supported languages like Python, Go, C#, etc.
- **OS**: Define whether the application runs on Linux or Windows.
- **instanceSize**: Predefined sizes for CPU and memory (`small`, `medium`, `large`).
- **environmentType**: Specifies the environment type (`dev`, `test`, `prod`).
- **replicas**: Set the desired number of application replicas (minimum 1).

### Example CRD Manifest

Here’s how you can define an application using the CRD:

```yaml
apiVersion: ci-cd.platform/v1
kind: ApplicationBuild
metadata:
  name: my-sample-app
spec:
  appId: "my-app"
  codeLanguage: "Python"
  OS: "Linux"
  instanceSize: "medium"
  environmentType: "dev"
  replicas: 2
```

Deploy this using `kubectl apply -f` and watch your custom CI/CD process unfold!

---

## 💡 CRD Example

Deploy a sample custom resource using the command:

```bash
kubectl apply -f examples/custom-resource-example.yaml
```

Check the status of the deployed resource:

```bash
kubectl get ApplicationBuild
```

---

## 🌍 Contributing

We welcome contributions from the DevOps community! Feel free to open issues, submit PRs, or suggest new features. Let’s work together to make CI/CD on Kubernetes even more powerful.

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/my-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/my-feature`
5. Open a pull request!

---


### 📣 Join the DevOps Conversation!

Connect with me on [LinkedIn](https://linkedin.com/in/vishalgunjal-) or explore more projects on [GitHub](https://github.com/vishalgunjalSWE). Let’s continue to push the boundaries of DevOps together! 💪