# Kubernetes / Docker Gaming Servers
## Use Docker to host Garry's Mod and Minecraft servers
## A Project by Ian and Wyatt

## Intro
After working tirelessly on Kubernetes, it was decided as a group to approach this project using Docker Swarm instead of Kubernetes. These Docker containers host Minecraft and Garry's Mod servers for access locally or over the internet.

## Why We Switched
Here is a short list of problems we encountered using Kubernetes:

In MiniKube:
-403 eror for settings and other menus
-Tried minikube with v 1.7.0 of kubernetes and the image wouldn't pull
-RBAC argument when creating minikube would error out and wouldn't launch kubernetes

In Kubernetes:
-Flannel version not compadible with kubernetes version
-Would not accept permissions for kubernetes-dashboard serviceaccount user, even though accepting the yaml file
-Kubernetes dashboard pod stuck at pending, fixed with taint command
-503 error when dashboard tried to load
-Once Kubernetes dashboard loaded. the dashboard wouldnt accept the token for the kubernetes-dashboard service account that was made admin
