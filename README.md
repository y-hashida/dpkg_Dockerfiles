# Dockerfile の書き溜め

## Docker イメージのビルド

```
## Ubuntu 18.04 (bionic)
$ docker build -t ubuntu_dpkg_build:bionic docker_bionic/
$ docker build -t ubuntu_dpkg_build_using_my_cache:bionic docker_bionic_using_apt-cacher-ng/

## Ubuntu 20.04 (focal)
$ docker build -t ubuntu_dpkg_build:focal docker_focal/
$ docker build -t ubuntu_dpkg_build_using_my_cache:focal docker_focal_using_apt-cacher-ng/
```

## Docker の起動

```
## Ubuntu 18.04 (bionic)
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build:bionic bash
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build_using_my_cache:bionic bash

## Ubuntu 20.04 (focal)
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build:focal bash
$ docker run --rm -it -v $(pwd):/opt/work -w /opt/work ubuntu_dpkg_build_using_my_cache:focal bash
```
