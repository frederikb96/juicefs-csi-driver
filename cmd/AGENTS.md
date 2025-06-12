This folder holds the Go entrypoints:

- `main.go` starts the CSI driver using the packages under `pkg/`.
- `controller.go`, `node.go` and `upgrade.go` implement command line flags for their respective modes.
- `dashboard/` contains the executable for the web dashboard.
