# flux-testing
Repository intended to learn and practice FluxCD

```
export GITHUB_TOKEN=<your-token>

flux bootstrap github \
  --owner=aacecandev \
  --repository=flux-testing \
  --path=clusters/testing \
  --personal

kubectl create secret generic tf-aws-keys \
  -n flux-system \
  --from-literal=access-key=<your-access-key> \
  --from-literal=secret-key=<your-secret-key>
```

Technique

- Flux bootstrapped on k8s
- Install Weaveworks Terraform Controller via Helm
- Normal file layout
  - main.tf - variables.tf - outputs.tf
  - Function source in subdirectory
- Manual testing before commiting to Git
- Terraform manifest
