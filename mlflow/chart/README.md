# Helm Charts for MLFlow

## Introduction

- This Helm chart deploy mlflow-server in a Kubernetes cluster
- The source code of all Helm charts can be found on GitHub: https://github.com/mlops-for-all/helm-charts/mlflow

## Prerequisites

- Kubernetes v1.17 ~ v1.21
- Helm v3
- Dynamic Provisioning StorageClass

---

## Quick Start

### Add Helm Repository

helm repo add <TODO>

### Helm Install

helm install --create-namespace --namespace mlflow-system mlflow .

## Configuration

The following tables lists the configurable parameters of the mlflow chart and the default values

## References

- https://github.com/cetic/helm-mlflow
- https://github.com/at-gmbh/docker-mlflow-server
- https://github.com/lightbend/ML-metadata-tutorial

## License

Apache license
