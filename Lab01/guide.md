# Environment Setup
This lab will help you set up your development environment by forking the repository, starting a GitHub Codespace, and running a local Kubernetes cluster using minikube.

Key Objectives:
- Fork the workshop repository to your GitHub account
- Launch a GitHub Codespace development environment
- Start a minikube Kubernetes cluster
- Configure a keep-alive to prevent the Codespace from timing out

Table of Contents:
- [Environment Setup](#environment-setup)
  - [1. Fork GitHub Repo](#1-fork-github-repo)
  - [2. Start a Codespace](#2-start-a-codespace)
  - [3. Run minikube](#3-run-minikube)
  - [4. Run a keep alive for the codespace](#4-run-a-keep-alive-for-the-codespace)


## 1. Fork GitHub Repo

Go to this repo and fork it to your own GitHub account so you have full control over the CI/CD pipeline.

## 2. Start a Codespace

Start a GitHub Codespace on your forked repo.

## 3. Run minikube

```bash
minikube start --cpus 3 --memory 8g
```
Wait for minikube to be ready. Then run the follwing command to check nodes:

```bash
kubectl get nodes
```

You should see something like this:

```
NAME       STATUS   ROLES           AGE   VERSION
minikube   Ready    control-plane   12s   v1.31.0
```

## 4. Run a keep alive for the codespace

In a new terminal, run the following command to keep the codespace alive.

```bash
while true; do date; sleep 60; done
```

> You've reached the end of the lab.
