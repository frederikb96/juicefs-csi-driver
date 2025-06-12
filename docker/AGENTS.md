Dockerfiles and Makefile for building driver and mount images.
Targets include:
- `image-version` to build multi-arch release images with tagged JuiceFS mount images.
- `ce-image` and `ee-image` build the mount images themselves.
Used by CI workflow `version.yaml` for official releases.
