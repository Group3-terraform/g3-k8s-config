# Group3 Kubernetes Ingress & Services

This repository stores all Kubernetes manifests related to:
- Ingress (AWS ALB)
- Deployments for service-a, service-b, service-c
- Services (ClusterIP) for internal routing

## Folder Structure
k8s-ingress/
  ingress/ingress.yaml
  apps/service-a-deploy.yaml
  apps/service-a-svc.yaml
  apps/service-b-deploy.yaml
  apps/service-b-svc.yaml
  apps/service-c-deploy.yaml
  apps/service-c-svc.yaml

## Apply Ingress
kubectl apply -f ingress/ingress.yaml

## Apply All Services
kubectl apply -f apps/

## Verify
kubectl get ingress -n apps
kubectl get svc -n apps
kubectl get deploy -n apps
kubectl get pods -n apps

## Routing
/a  → service-a
/b  → service-b
/c  → service-c
