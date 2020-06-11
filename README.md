# Dockerfile の書き溜め

## Docker イメージのビルド

```
## Ubuntu 18.04 (bionic)
$ docker build -t ubuntu_dpkg_build:bionic docker_bionic/

## Ubuntu 20.04 (focal)
$ docker build -t ubuntu_dpkg_build:focal docker_focal/
```

## Docker の起動

```
## Ubuntu 18.04 (bionic)
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build:bionic bash

## Ubuntu 20.04 (focal)
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build:focal bash
```
