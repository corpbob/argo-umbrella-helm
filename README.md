# Umbrella Helm Chart Demo

This is a demo showcasing the installation of an application using the umbrella pattern of Helm chart.

## Installation

1. The Helm chart is located inside the `charts` directory.

2. There are separate values files for development and production environments.

3. To configure a particular chart in the `values.yaml` file, the configuration should be under the chart name. For example, to configure 1 replica for the `hello-world` chart, the values file would look like:

```yaml
hello-world:
  replicaCount: 1
```

## Deployment with ArgoCD

Use the manifest file `apps-umbrella-chart.yaml` to create the application in ArgoCD using the following command:

```bash
kubectl apply -f apps-umbrella-chart.yaml
```

Or you can also deploy the specific environment. For example, to deploy the dev environment:

```bash
kubectl apply -f apps/app-dev.yaml
```

Ensure you have ArgoCD installed and configured in your Kubernetes cluster before applying the manifest file.



