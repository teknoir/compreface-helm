# CompreFace Helm Chart

This chart deploys the CompreFace to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the CompreFace to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: compreface
  namespace: default
spec:
  repo: https://teknoir.github.io/compreface-helm
  chart: compreface
  targetNamespace: default
  valuesContent: |-
    
```


## Adding the repository

```bash
helm repo add teknoir-compreface https://teknoir.github.io/compreface-helm/
```

## Installing the chart

```bash
helm install compreface teknoir-compreface/compreface -f values.yaml
```