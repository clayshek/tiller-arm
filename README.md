# tiller-arm
Dockerfile for Tiller (Helm server) on ARM

## Summary

Docker image for Tiller (Helm server) for ARM architecture (Raspberry Pi), on alpine. Tested working on Raspberry Pi 3 / Stretch. Base image size is roughly 126 MB. Based off of https://github.com/ljfranklin/helm-arm.

## Usage

Run helm init, using the <a href="https://cloud.docker.com/repository/docker/clayshek/tiller-arm">clayshek/tiller-arm</a> Docker image, or first clone this repo, modify Dockerfile as desired, then build and push new image to use with helm init. 

Prerequisite: Requires configuring Kubernetes <a href="https://docs.helm.sh/using_helm/#role-based-access-control">RBAC for Tiller service account</a>. 

Example:

`helm init --tiller-image=clayshek/tiller-arm --service-account tiller`

## To-Do

 - [ ] Better versioning & image tagging
