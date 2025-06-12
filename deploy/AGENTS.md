Kustomize manifests used to generate installation YAML.

Subfolders:
- `kubernetes/base` contains base resources for the CSI driver.
- `kubernetes/release` overlays used by `make yaml` to build `deploy/k8s.yaml`.
- `kubernetes/webhook*` overlays enabling the admission webhook.
Generated YAML is stored in `deploy/k8s.yaml` and webhook files.
