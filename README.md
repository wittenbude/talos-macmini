# talos-macmini

This repository contains an automated Talos build that implements a fix for https://github.com/siderolabs/talos/issues/13231. The generated images are able to run on Intel Macs.

## Usage

The build is fully automated in a GitHub Actions workflow. Version updates are handled by Renovate. To build a release for a new version, do the following:

1. Renovate should create a PR to bump the git submodules to their latest versions. Merge the PR.
2. Create a new release in this repository. The GitHub Actions workflow will automatically build the release and upload the artifacts to the release page.

The workflow will also publish OCI images to the GitHub container registry so you can use the built-in Talos update mechanism with the published images.

## Extensions

Currently the build contains the following Talos extensions:

- iscsi-tools

## References

The implementation builds on the previous results:

- [Talos in Intel Mac](https://github.com/aliAljaffer/homelab/blob/main/docs/talos-intel-mac.md)
- [talos-builder](https://github.com/talos-rpi5/talos-builder/tree/main)
