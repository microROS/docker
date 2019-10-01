# Docker

This repository contains docker-related material to setup, configure and develop with [micro-ROS](https://microros.github.io/)
These set of dockerfiles provide ready-to-use environments and applications.
The docker images can be found in [dockerhub](https://hub.docker.com/u/microros).

Avaiable images are listed below:

| Image | Description |
|-------|-------------|
| Base  | Base image with ROSDISTRO installation + micro-ROS specific build system. Used as base of any other micro-ROS image |
| micro-ROS-Agent | Image containing a pre-compiled micro-ROS-Agent, ready to use as standalone application |
| micro-ROS-demos | Contains precompiled micro-ROS-demos, ready to use to view micro-ROS funcionality |
| micro-ROS-firmware | Contains a firmware ws ready to configure and build micro-ROS |
| micro-ROS-Olimex-NuttX | Contains a ready to flash example for  Olimex STM32 E407 |

Image hiearchy

Base
|-- micro-ros-agent
|-- micro-ros-demos
|-- firmware
    |-- micro-ROS-Olimex-NuttX


## Pre-requisite

You need to have docker in your system.
For installing docker, refer to https://www.docker.com/.

## Automated builds

These Docker files are used for automatically create images on Docker Hub.
These builds are tagged as the ROS 2 version they will be compatible with: eg. crystal, dashing...
The latest tag will be always the latest release of ROS 2.

These automatic builds has direct relation with the conten of the micro-ROS repositories:

| Image | Triggers |
|-------|----------|
| Base | micro-ROS/micro-ROS-build |
| Firmware | micro-ROS/apps micro-ROS/NuttX |
| micro-ROS-Agent | |
| micro-ROS-Olimex-NuttX |  | 

Apart from gihub repositoriesi changes, a build is triggered whenever the base image is updated on Docker Hub.
Base images are specified in the FROM: directive in the Dockerfile.

## Status

Images are automatically build in dockerhub, here you can find the current status of each image

**Base:** [![Docker Automated build](https://img.shields.io/docker/automated/microros/base.svg?logo=docker)](https://hub.docker.com/r/microros/base/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/microros/base.svg?logo=docker)](https://hub.docker.com/r/microros/base/)
[![Compare Images](https://images.microbadger.com/badges/image/microros/base.svg)](https://microbadger.com/images/microros/base)

**micro-ROS-Agent:** [![Docker Automated build](https://img.shields.io/docker/automated/microros/micro-ros-agent.svg?logo=docker)](https://hub.docker.com/r/microros/micro-ros-agent/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/microros/micro-ros-agent.svg?logo=docker)](https://hub.docker.com/r/microros/micro-ros-agent/)
[![Compare Images](https://images.microbadger.com/badges/image/microros/micro-ros-agent.svg)](https://microbadger.com/images/microros/micro-ros-agent)

**micro-ROS-demos:** [![Docker Automated build](https://img.shields.io/docker/automated/microros/micro-ros-demos.svg?logo=docker)](https://hub.docker.com/r/microros/micro-ros-demos/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/microros/micro-ros-demos.svg?logo=docker)](https://hub.docker.com/r/microros/micro-ros-demos/)
[![Compare Images](https://images.microbadger.com/badges/image/microros/micro-ros-demos.svg)](https://microbadger.com/images/microros/micro-ros-demos)

**firmware:** [![Docker Automated build](https://img.shields.io/docker/automated/microros/firmware.svg?logo=docker)](https://hub.docker.com/r/microros/firmware/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/microros/firmware.svg?logo=docker)](https://hub.docker.com/r/microros/firmware/)
[![Compare Images](https://images.microbadger.com/badges/image/microros/firmware.svg)](https://microbadger.com/images/microros/firmware)

