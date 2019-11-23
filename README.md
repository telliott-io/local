# Local Development

This repo contains setup and useful information for local development.

# Tilt

[Tilt](https://tilt.dev) is a tool for locally running Kubernetes projects. It allows you to configure a fast feedback loop with automatic build and deploy when you make changes to your code.

This repo contains a Tiltfile that consolidates all project Tiltfiles to run all projects at once, assuming all repos are in a common parent directory.

# Docker for Desktop

Docker for Desktop contains its own Kubernetes setup which is more than sufficient for testing of these projects.

Minikube may also be used if desired, but Docker for Desktop is recommended.

## RBAC

Docker for Desktop uses RBAC, but by default has a Role Binding that gives all accounts admin permissions.

In order to effectively test RBAC configurations locally, you can remove this binding:

```
$ kubectl delete clusterrolebinding/docker-for-desktop-binding
```

The yaml for this binding as at November 23 2019 can be found in `docker-for-desktop.yaml`.# local
