# Layer Image Environment Deploy

Kaptain config layer providing common docker build settings for all image-environment-deploy images.

Projects that reference this layer inherit:

- **Multi-arch docker builds** — linux/amd64 and linux/arm64
- **Dockerfile in src/docker** — single path for both architectures
- **Compound versioning** — version derived from kaptain-deploy-scripts and base image versions (6 part max)
- **Post-build docker test hook** — runs validate-tooling inside the built image for each platform
- **Additional release branches** — main-1.32 through main-1.40
- **Layer payload** — delivers test-docker-image.bash to kaptain-out/ for the post-build hook
