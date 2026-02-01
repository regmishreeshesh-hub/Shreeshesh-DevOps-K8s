# DevOps Portfolio - Kubernetes Manifests

## Overview
This directory contains the Kubernetes manifests for deploying the DevOps Engineer portfolio website.

## Files
- `01-namespace.yaml` - Creates the nginx-devops namespace
- `02-configmap.yaml` - Contains the HTML content for the portfolio website
- `03-deployment.yaml` - Nginx deployment configuration
- `04-service.yaml` - NodePort service to expose the website

## Deployment
Apply all manifests in order:
```bash
kubectl apply -f devops/
```

Or apply individually:
```bash
kubectl apply -f 01-namespace.yaml
kubectl apply -f 02-configmap.yaml
kubectl apply -f 03-deployment.yaml
kubectl apply -f 04-service.yaml
```

## Access
The website will be available at:
- NodePort: `http://<node-ip>:30001`
- Port-forward: `kubectl port-forward svc/nginx-devops -n nginx-devops 8080:80`

## Features
- **Responsive Design**: Works on all screen sizes
- **Interactive Skills**: Click to expand skill categories
- **Animated UI**: Floating particles and smooth transitions
- **Modern Styling**: Gradient backgrounds and glass morphism effects
- **Contact Information**: Email and phone display
# Shreeshesh-DevOps-K8s
