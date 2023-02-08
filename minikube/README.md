# Minikube hands-on

The purporse here is to guide you through the installation steps for minikube and deploy a simple nginx page as result.

## Minimum requirements

- 2 CPUs or more
- 2GB of free memory
- 20GB of free disk space
- Internet connection

## Getting Started

### All you need

- Docker installed

### Installing

This installation is using the package manager for windows Chocolatey. <br>
In case you don't have it installed visit: https://docs.chocolatey.org/en-us/choco/setup

```bash
choco install minikube
```

```bash
choco install kubernetes-cli
```

### Executing program

- How to run the program
- Step-by-step bullets

```
code blocks for commands
```

```
Exiting due to PR_HYPERV_MODULE_NOT_INSTALLED: Failed to start host: creating host: create: precreate: Hyper-V PowerShell Module is not available
```

```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V-Tools-All -All
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
