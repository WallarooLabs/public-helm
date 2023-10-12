# Wallaroo Model Serving Engine Helm Chart

This helm chart deploys Wallaroo Model Serving Engine. It draws both models and container images
from an OCI registry, configured below.

## Installation

1. Create a file called, for example, `local-values.yaml`, which overrides the chart's `values.yaml`.
The `ociRegistry` overrides are mandatory; anything else is optional.

```yaml
ociRegistry:
  registry: "oci.bigcorp.io"
  username: "joe_data"
  password: "your_secret_here"

engine:
  cpus: 1
```

2. Perform the helm installation.

```sh
helm install --create-namespace --namespace your_ns --values local-values.yaml release1 .
```
