# DevContainer for kubebuidler operator development

This devcontainer is based on the [alpine golang 1.17](https://hub.docker.com/_/golang) docker image.

## Intoduction

This repo contains a [DevContainer](https://code.visualstudio.com/docs/remote/containers) used and coupled with Visual Studio Code.

When developing operators `kubebuidler` is a very broad and used tool, but it runs on linux systems exlusivly, so as part of development using a devcontainer could give a more natural flow to the operator development using `kubebuilder`.

It automatically comes with all your kubebuilder needs and golang 1.17 and some Visual Studio Code extensions for operator development on k8s.

## What is a part of the devcontainer

This devcontainer uses a `Dockerfile`, it bundles up the basic prerequisites to develop operators using `kubebuidler`:

* `go` version v1.16+
* `docker` version 17.03+
* `kubectl` version v1.11.3+
* `kubebuilder` version v3.1+
* `kustomize` version v2.0
* `controller-gen` version v0.7.0

Other than that the devcontainer also comes with:

* `helm` version v3
* `git` version 2.34.1

## Working with kubebuidler

When working with kubebuilder its recommended reading [the kubebuilder book](https://book.kubebuilder.io/).
