# Docker Image Packaging for Nix

<img src="/alvistack.svg" width="75" alt="AlviStack">

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-nix/master)](https://gitlab.com/alvistack/docker-nix/-/pipelines)
[![GitHub tag](https://img.shields.io/github/tag/alvistack/docker-nix.svg)](https://github.com/alvistack/docker-nix/tags)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-nix.svg)](https://github.com/alvistack/docker-nix/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/nix-2.3.svg)](https://hub.docker.com/r/alvistack/nix-2.3)

This image contains an installation of the Nix package manager.

Learn more about Nix: <https://nixos.org/>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/nix-2.3`](https://hub.docker.com/r/alvistack/nix-2.3)
      - [`packer/docker-2.3/packer.json`](https://github.com/alvistack/docker-nix/blob/master/packer/docker-2.3/packer.json)

## Overview

This Docker container makes it easy to get an instance of nix up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

Start Nix:

    # Pull latest image
    docker pull alvistack/nix-2.3
    
    # Run as detach
    docker run \
        -itd \
        --name nix \
        --volume ${PWD}:${PWD} \
        --workdir ${PWD} \
        alvistack/nix-2.3

**Success**. Nix is now available.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-nix/tags) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-nix/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
