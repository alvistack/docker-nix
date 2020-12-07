# Docker Image Packaging for Nix

[![Travis](https://img.shields.io/travis/com/alvistack/docker-nix.svg)](https://travis-ci.com/alvistack/docker-nix)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-nix.svg)](https://github.com/alvistack/docker-nix/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-nix.svg)](https://github.com/alvistack/docker-nix/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/nix.svg)](https://hub.docker.com/r/alvistack/nix/)

This image contains an installation of the Nix package manager.

Learn more about Nix: <https://nixos.org/>

## Supported Tags and Respective Packer Template Links

  - [`2.3`, `latest`](https://github.com/alvistack/docker-nix/blob/master/packer/docker-2.3/packer.json)

## Overview

This Docker container makes it easy to get an instance of nix up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

Start Nix:

    # Pull latest image
    docker pull alvistack/nix
    
    # Run as detach
    docker run \
        -itd \
        --name nix \
        --volume ${PWD}:${PWD} \
        --workdir ${PWD} \
        alvistack/nix

**Success**. Nix is now available.

## Versioning

### `alvistack/nix:latest`

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-nix/releases) of this repository. Thus using `alvistack/nix:latest` or `alvistack/nix` will ensure you are running the most up to date stable version of this image.

### `alvistack/nix:<version>`

The version tags are rolling release rebuild by [Travis](https://travis-ci.com/alvistack/docker-nix) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
