# Terraform Kubernetes Cloud Deployment

A DevOps project that demonstrates Infrastructure as Code using Terraform and deployment of a containerized application using Docker and Kubernetes.

## 📌 Project Overview

The Terraform Kubernetes Cloud Deployment project demonstrates how cloud infrastructure and application deployment can be automated using modern DevOps tools.

Terraform is used to define and provision cloud infrastructure using Infrastructure as Code. Docker is used to package the application and its dependencies into a container, while Kubernetes is used to deploy, manage, and scale the containerized application.

The project demonstrates the integration of Terraform, AWS, Docker, Kubernetes, Git, and GitHub in a cloud-based application deployment workflow.

## 🚀 Key Features

- 🏗️ Defines infrastructure using Terraform.
- 💻 Demonstrates Infrastructure as Code (IaC).
- ☁️ Provisions cloud infrastructure on AWS.
- 🐳 Containerizes the application using Docker.
- 📦 Packages the application and its dependencies into a Docker image.
- ☸️ Deploys the containerized application using Kubernetes.
- 🔄 Manages application containers using Kubernetes Deployments.
- 🌐 Exposes the application using a Kubernetes Service.
- 📈 Supports application scaling using Kubernetes.
- ⚙️ Demonstrates repeatable infrastructure provisioning and application deployment.

## 🛠️ Technologies Used

- **Terraform**
- **AWS**
- **Docker**
- **Kubernetes**
- **kubectl**
- **Git**
- **GitHub**
- **Python**
- **Flask**

## 🔄 Workflow

```text
Application Code
     ↓
Dockerfile
     ↓
Docker Image
     ↓
Docker Hub / Container Registry
     ↓
Terraform
     ↓
Provision Cloud Infrastructure
     ↓
Kubernetes Environment
     ↓
Kubernetes Deployment
     ↓
Kubernetes Pods
     ↓
Kubernetes Service
     ↓
Application Access
```

## 📂 Project Structure

```text
Terraform-Kubernetes-Deployment/
│
├── app/
│   └── app.py
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── kubernetes/
│   ├── deployment.yaml
│   └── service.yaml
│
├── Dockerfile
├── requirements.txt
└── README.md
```

## ⚙️ Requirements & Setup

Before running the project, make sure the following are installed and configured:

- **Git**
- **GitHub Account**
- **Python**
- **Docker**
- **Docker Hub Account or Container Registry**
- **Terraform**
- **AWS Account**
- **AWS CLI**
- **Kubernetes**
- **kubectl**

## 📥 Setup

- Clone this repository:

```bash
git clone https://github.com/SciddhantoSinha/Terraform-Kubernetes-Deployment.git
```

- Navigate to the project directory:

```bash
cd Terraform-Kubernetes-Deployment
```

- Configure your AWS credentials.

- Make sure Docker is installed and running.

- Install Terraform.

- Install and configure Kubernetes and `kubectl`.

- Build the application Docker image and push it to a container registry before deploying the application.

## ▶️ How to Run

### Install Python Dependencies

Install the required application dependencies:

```bash
pip install -r requirements.txt
```

### Run the Application Locally

Run the Python application:

```bash
python app/app.py
```

The application can be accessed locally at:

```text
http://localhost:5000
```

### Build the Docker Image

Build the Docker image:

```bash
docker build -t terraform-kubernetes-app .
```

### Run the Docker Container

Run the application inside a Docker container:

```bash
docker run -p 5000:5000 terraform-kubernetes-app
```

The containerized application can be accessed at:

```text
http://localhost:5000
```

### Initialize Terraform

Navigate to the Terraform directory:

```bash
cd terraform
```

Initialize Terraform:

```bash
terraform init
```

### Validate the Terraform Configuration

Check whether the Terraform configuration is valid:

```bash
terraform validate
```

### Check the Terraform Execution Plan

View the infrastructure resources that Terraform plans to create:

```bash
terraform plan
```

### Provision the Infrastructure

Create the cloud infrastructure:

```bash
terraform apply
```

Type `yes` when Terraform asks for confirmation.

### Deploy the Application to Kubernetes

Navigate back to the project root directory and apply the Kubernetes Deployment:

```bash
kubectl apply -f kubernetes/deployment.yaml
```

Create the Kubernetes Service:

```bash
kubectl apply -f kubernetes/service.yaml
```

### Check Running Kubernetes Pods

```bash
kubectl get pods
```

### Check Kubernetes Deployments

```bash
kubectl get deployments
```

### Check Kubernetes Services

```bash
kubectl get services
```

## 📊 Infrastructure and Deployment Process

The project follows the following workflow:

1. The application is developed using Python and Flask.
2. Docker packages the application and its dependencies into a container image.
3. The Docker image is stored in a container registry.
4. Terraform defines the required cloud infrastructure using code.
5. Terraform provisions the required infrastructure on AWS.
6. Kubernetes deploys the containerized application.
7. Kubernetes creates and manages the application Pods.
8. A Kubernetes Service exposes the application.
9. Kubernetes can scale the application by increasing the number of running Pods.

## 🏗️ Infrastructure as Code

Terraform is used to manage infrastructure using configuration files instead of manually creating cloud resources.

The Terraform workflow follows:

```text
Terraform Configuration
        ↓
terraform init
        ↓
terraform validate
        ↓
terraform plan
        ↓
terraform apply
        ↓
AWS Infrastructure Created
```

This approach makes infrastructure provisioning more consistent, repeatable, and easier to manage.

## ☸️ Kubernetes Deployment

Kubernetes is used to manage the containerized application.

The Kubernetes Deployment:

- Defines the application container.
- Specifies the required number of application replicas.
- Creates and manages Pods.
- Recreates failed Pods when required.
- Supports application scaling.

The Kubernetes Service:

- Provides network access to the application.
- Allows communication with the application Pods.
- Provides a stable endpoint for accessing the application.

## 📈 Application Scaling

Kubernetes allows the application to scale by increasing the number of running Pods.

For example:

```bash
kubectl scale deployment <deployment-name> --replicas=3
```

This increases the number of application instances to three Pods.

## 🎯 Use Case

This project demonstrates a cloud-native application deployment workflow.

It can be used as a reference for understanding how Infrastructure as Code, containerization, and container orchestration work together to deploy applications in a cloud environment.

The project represents a common DevOps workflow where infrastructure is provisioned using code and applications are deployed and managed using containers and Kubernetes.

## 💡 Benefits

- Reduces manual infrastructure configuration.
- Automates cloud infrastructure provisioning.
- Provides repeatable infrastructure using Terraform.
- Packages applications consistently using Docker.
- Simplifies container management using Kubernetes.
- Supports application availability and scaling.
- Makes infrastructure easier to reproduce.
- Demonstrates a complete cloud-based application deployment workflow.

## 🔐 Security Considerations

AWS credentials and other sensitive information should not be stored directly in the source code.

Sensitive configuration values should be managed using:

- Environment variables.
- AWS IAM roles and permissions.
- Secret management services.
- Secure credential management mechanisms.

Terraform state files may also contain sensitive infrastructure information and should be managed securely.

## 📚 Key Learnings

- Understanding Infrastructure as Code (IaC).
- Provisioning infrastructure using Terraform.
- Understanding Terraform providers, resources, and state files.
- Containerizing applications using Docker.
- Building and managing Docker images.
- Understanding Kubernetes Pods.
- Creating Kubernetes Deployments.
- Exposing applications using Kubernetes Services.
- Managing and scaling containerized applications.
- Understanding cloud-based application deployment.
- Integrating Terraform, Docker, Kubernetes, and AWS.

## 👨‍💻 Author

**Sciddhanto Sinha**

B.Tech – Computer Science Engineering (AI & Analytics)
