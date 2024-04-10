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

**_NOTE_**: You'll need a GitHub Personal Access Token with `administration:write`, `contents:write`, `commit-status:write`, `metadata:read` on this repository

```sh
flux --context kind-flux-and-flagger-demo bootstrap github --owner elliottpope --path local --private --personal --read-write-key --reconcile --repository flux-and-flagger-demo --branch main --components-extra image-automation-controller,image-reflector-controller 
```