# regctl-docker

Unofficial multiarch docker image for [regclient](https://github.com/regclient/regclient), client interface for the container registry API.
This includes [regctl](https://github.com/regclient/regclient/blob/main/docs/regctl.md) for a command line interface to manage registries, but also [regsync](https://github.com/regclient/regclient/blob/main/docs/regsync.md) and [regbot](https://github.com/regclient/regclient/blob/main/docs/regbot.md).

Get it from GitHub container registry as

`docker pull ghcr.io/davidecavestro/regctl:latest`

or from dockerhub as

`docker pull davidecavestro/regctl:latest`

## Usage

THe default
You can test it with a public registry, i.e. the following command
`docker run --rm -it davidecavestro/regctl tag ls davidecavestro/regctl`
will provide the list of published tags.