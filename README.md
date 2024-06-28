# regctl-docker

Unofficial multiarch docker image for [regclient](https://github.com/regclient/regclient), client interface for the container registry API.
This includes [regctl](https://github.com/regclient/regclient/blob/main/docs/regctl.md) for a command line interface to manage registries, but also [regsync](https://github.com/regclient/regclient/blob/main/docs/regsync.md) and [regbot](https://github.com/regclient/regclient/blob/main/docs/regbot.md).

Get it from GitHub container registry as

`docker pull ghcr.io/davidecavestro/regctl:latest`

or from dockerhub as

`docker pull davidecavestro/regctl:latest`


## Usage

You can test it with a public registry, i.e. the following command
`docker run --rm -it davidecavestro/regctl tag ls davidecavestro/regctl`
will provide the list of published tags.


## Why

Why another `regctl` image given that there's [the official one](https://github.com/regclient/regclient/blob/main/docs/install.md#running-as-a-container)?
The official image is usually preferable but it lacks the `sleep` executable, making it hard to use for CI - namely on a k8s pod - where the container should simply wait for commands.

Hence this image, built on alpine/debian/busybox variants.