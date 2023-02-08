# Minikube hands-on

The purporse here is to guide you through the installation steps for minikube, deploy nginx, nginx service, ingress and visualize it.

## Minimum requirements

- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection

## Getting Started

### Installing

This installation is using the package manager for windows called **Chocolatey**. <br>
For any other distributions you can follow here: https://minikube.sigs.k8s.io/docs/start/ <p>
In case you don't have **Chocolatey** installed visit: https://docs.chocolatey.org/en-us/choco/setup and install before to continue with the below steps.

```
choco install minikube
```

```
choco install kubernetes-cli
```

### Initializing

```
minikube start
```

## For Windows users, in case you get the following error:

```
Exiting due to PR_HYPERV_MODULE_NOT_INSTALLED: Failed to start host: creating host: create: precreate: Hyper-V PowerShell Module is not available
```

Open a PowerShell with Admin privileges and run the command below to enable HYPERV MODULE.

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All
```

### Feeling at home

```
kubectl help
```

```
kubectl get nodes
```

```
kubectl get ns
```

```
kubectl config current-context
```

### Deploying nginx deployment component

```
kubectl create namespace random-namespace
```

```
kubectl apply -f nginx/nginx1-deployment.yaml -n random-namespace
```

```
kubectl apply -f nginx/nginx1-service.yaml -n random-namespace
```

```
kubectl port-forward service/nginx1-service 8080:8080 -n random-namespace
```

```
kubectl apply -f nginx/nginx2-deployment.yaml -n random-namespace
```

```
kubectl apply -f nginx/nginx2-service.yaml -n random-namespace
```

```
kubectl port-forward service/nginx2-service 8080:8080 -n random-namespace
```

#### Let's be curious

```
kubectl get pods -n random-namespace
```

```
kubectl get deployment -n random-namespace
```

```
kubectl describe deployment/nginx1-deployment -n random-namespace
```

```
kubectl describe service nginx1-service -n random-namespace
```

### Minikube dashboards

```
minikube dashboard
```

### Ingress is your friend

```
minikube addons enable ingress
```

```
kubectl apply -f ingress.yaml -n nginx
```

```
kubectl apply -f deployment.yaml -n nginx
```

```
kubectl apply -f service.yaml -n nginx
```

### Happy Helm Charts

```
choco install kubernetes-helm
```

```
kubectl create namespace grafana
```

```
helm repo add grafana https://grafana.github.io/helm-charts
```

```
helm install grafana grafana/grafana -n nginx
```

```
kubectl port-forward service/grafana 9090:80 -n grafana
```

<p>

## Author

Anderson Soares Lopes

[![GitHub](https://skillicons.dev/icons?i=github)](https://github.com/lopes221)
[![Linkedin](https://skillicons.dev/icons?i=linkedin)](https://www.linkedin.com/in/andersonsoaresl/)

## Document Version History

- 0.1
  - Initial Release

## References

- https://minikube.sigs.k8s.io/docs/start/
- https://docs.chocolatey.org/en-us/choco/setup
- https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/#install-nonstandard-package-tools
- https://kubernetes.io/docs/concepts/workloads/controllers/deployment/
- https://kubernetes.io/docs/concepts/services-networking/service/
- https://helm.sh/
- https://minikube.sigs.k8s.io/docs/
- https://minikube.sigs.k8s.io/docs/faq/
