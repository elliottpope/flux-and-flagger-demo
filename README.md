# Flux/Flagger Demo

## Set Up

### Prerequisites

- Podman (version `>= 5.0.1`)
- Kind (version `>= 0.22.0`)
- Flux CLI (version `>= 2.2.3`)

### Run a Kind Cluster

```sh
KIND_EXPERIMENTAL_PROVIDER=podman kind create cluster --config kind.yaml
```

### Bootstrap Flux

