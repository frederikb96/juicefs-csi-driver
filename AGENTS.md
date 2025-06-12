JuiceFS CSI Driver repository overview:

- `cmd/` contains Go entrypoints for the controller, node and dashboard binaries.
- `pkg/` hosts the main Go packages. See individual `AGENTS.md` files inside for details.
- `deploy/` keeps kustomize manifests used to generate `deploy/k8s.yaml` and webhook manifests.
- `docker/` contains Dockerfiles and a Makefile used to build release images.
- `dashboard-ui-v2/` is the frontend project for the dashboard.
- `.github/` holds CI workflows. `version.yaml` builds and pushes release images.

The official Helm chart is **not** stored in this repo. It lives in
<https://github.com/juicedata/charts> under `charts/juicefs-csi-driver`.
Run `curl` to fetch `values.yaml` if you need to inspect default options.

To build Kubernetes manifests run `make yaml`. To build images run
`make -C docker image-version` (used by `.github/workflows/version.yaml`).
Publishing a new Helm version requires updating the chart repository with the
new image tags produced by the `version` workflow.
