# Falco K8s Mini Project (Learning Story)

This repository is used as a **learning curve to understand a bit about Falco** and how it integrates with Kubernetes.  
I followed a step-by-step guide and captured screenshots of the process for my own reference.

## Very short: How Falco connects with Kubernetes
Falco runs as a privileged sensor (via kernel module or eBPF) on each Linux node, capturing syscalls and container metadata. It deploys as a DaemonSet in Kubernetes and generates alerts when activities match predefined security rules.

## Repository contents
- `images/` → five screenshots (Image-001 through Image-005) showing my steps.
- `README.md` → this explanation and notes.

## Screenshots
![Image 1](images/Image-001.png)  
![Image 2](images/Image-002.png)  
![Image 3](images/Image003.png)  
![Image 4](images/Image-004.png)  
![Image 5](images/Image-005.png)

## Walkthrough Guide
See `walkthrough/Falco-K8s-Guide.md` for Steps 2 → 5 and sample files.
