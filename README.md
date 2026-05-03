# AutoNode 🚀  
### Efficient Deployment & System Package Management using Ansible

---

## 📌 Introduction

AutoNode is a DevOps automation project designed to simplify and standardize server setup, package management, and application deployment using Ansible.

The project follows Infrastructure as Code (IaC) principles to automate repetitive system administration tasks and ensure consistent deployment across environments.

---

## ❗ Problem Statement

In traditional system administration, deploying applications and configuring servers manually creates several challenges:

### 🔴 Key Issues:
- Manual installation of packages leads to inconsistency
- High chances of human error during configuration
- Time-consuming setup process
- Difficult to replicate environments across multiple systems
- Lack of scalability in deployment
- Complex dependency management
- Service misconfiguration (NGINX, Node, etc.)

For example, installing Node.js, setting up NGINX, configuring firewall rules, and deploying an app manually can take hours and still be error-prone.

---

## 💡 Proposed Solution

AutoNode solves these issues by automating the entire workflow using Ansible.

### ✔ What AutoNode Does:
- Automates system updates and package installation
- Installs and configures Node.js environment
- Sets up Docker (for container readiness)
- Configures firewall rules securely
- Deploys Node.js application automatically
- Uses PM2 to manage application processes
- Configures NGINX as a reverse proxy
- Ensures services restart properly

---

## 🎯 Objectives

- Reduce manual server configuration effort
- Provide consistent deployment across systems
- Automate package management
- Enable scalable and repeatable infrastructure setup
- Demonstrate real-world DevOps practices

---

## 🏗️ System Architecture
---

## ⚙️ Technologies Used

### 🔹 Ansible
- Core automation tool
- Executes playbooks to configure systems
- Agentless architecture (no installation required on target machines)

### 🔹 Node.js
- Backend application runtime
- Lightweight server used for deployment demonstration

### 🔹 NGINX
- Reverse proxy server
- Handles incoming HTTP requests and forwards to Node app

### 🔹 Docker
- Containerization platform
- Installed for future scalability and container-based deployment

### 🔹 PM2
- Process manager for Node.js
- Keeps application running continuously
- Enables restart and monitoring

### 🔹 UFW (Uncomplicated Firewall)
- Security tool for managing firewall rules
- Allows controlled access (HTTP, SSH)

---

## 🔄 Workflow (Step-by-Step Execution)

1. User runs deployment script
2. Ansible connects to the target system
3. System packages are updated
4. Required tools are installed (Git, Curl, NGINX, etc.)
5. Node.js is installed and configured
6. Docker is installed and started
7. Firewall rules are applied (SSH, HTTP allowed)
8. Application files are copied to server
9. Dependencies are installed using npm
10. Application is started using PM2
11. NGINX is configured as reverse proxy
12. Services are restarted and verified

---

## 📂 Project Structure

autonode/
│── README.md
│── .gitignore
│── requirements.txt
│
├── ansible/
│   ├── inventory.ini
│   ├── playbook.yml
│   ├── vars.yml
│
├── app/
│   ├── package.json
│   └── server.js
│
├── configs/
│   └── nginx.conf
│
└── scripts/
    └── deploy.sh
