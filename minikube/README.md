# Minikube hands-on

The purporse here is to guide you through the installation steps for minikube, deploy nginx, nginx service and visualize.

## Minimum requirements

- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection

## Getting Started

### Installing

This installation is using the package manager for windows called **Chocolatey**. <br>
For any other distributions you can follow here: https://minikube.sigs.k8s.io/docs/start/ <p>
In case you don't have **Chocolatey** installed visit: https://docs.chocolatey.org/en-us/choco/setup and install before to continue as below.

```bash
choco install minikube
```

```bash
choco install kubernetes-cli
```

### Initializing

```bash
minikube start
```

## For Windows users, in case you get the following error:

```
Exiting due to PR_HYPERV_MODULE_NOT_INSTALLED: Failed to start host: creating host: create: precreate: Hyper-V PowerShell Module is not available
```

Run the command below to enable HYPERV MODULE.

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All
```

### Feeling at home

```bash
kubectl help
```

```bash
kubectl get nodes
```

```bash
kubectl get ns
```

```bash
kubectl config current-context
```

### Deploying nginx

```bash
kubectl apply -f <something-here>
```

```
code blocks for commands
```

## Find more here

Minikube project documentation page

https://minikube.sigs.k8s.io/docs/

Minikube FAQ

https://minikube.sigs.k8s.io/docs/faq/

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
