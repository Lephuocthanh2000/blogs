# Kubernetes Cluster Setup with Kubeadm

**Date:** 2024-12-21T20:53:29+07:00  
**Draft:** true  

## Introduction

In this guide, I will walk you through setting up a Kubernetes (K8s) cluster using `kubeadm`, a tool that simplifies the process of creating Kubernetes clusters. This approach is ideal for those who want to manually set up their clusters with full control over the environment.

## Prerequisites

Before you begin, ensure the following:

- **Two or more nodes:** You will need at least one master node and one worker node. These can be physical or virtual machines.
- **Linux-based OS:** Ubuntu 20.04 or CentOS 7/8 is preferred for compatibility.
- **Root/Sudo privileges:** Ensure you have root or sudo privileges on all nodes.
- **Swap is disabled:** Kubernetes recommends disabling swap on all nodes.
- **Firewall settings:** Allow communication between the nodes over specific ports (e.g., 6443, 10250, 10251, 10252, etc.).

## Step 1: Prepare the Nodes

### 1.1 Update the System

On all nodes (master and worker), run the following commands to update the system:

```bash
sudo apt update && sudo apt upgrade -y
```
### 1.2 Install required packages:
```bash
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

