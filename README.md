# rhubarb-pi

This repo contains a collection of code to help build a Kubernetes cluster
on Raspberry Pi Compute Modules. Specifically, this is targeted toward Compute
Module 3+ boards, and is tested on a Turing Pi v1 cluster.

The project was bred to help bring together various missing pieces required
to get a Homelab running on CM3+ cluster.

It's inspired by the work of [HypriotOS](https://github.com/hypriot/image-builder-rpi)
and [DieterReuter's Workshop](https://github.com/DieterReuter/workshop-raspberrypi-64bit-os).

However, another goal is to reduce the complexity while making this work also
educational. To that end, the goal is not to support every chip and board, but
specifically the arm8 architecture on the Raspberry Pi CM3+ Broadcom chips.

## Resources

* Raspberry Pi's [Linux Kernel Documentation](https://github.com/hypriot/image-builder-rpi)
* [Image Builder RPI 64](https://github.com/DieterReuter/image-builder-rpi64)
* [DieterReuter's Workshop](https://github.com/DieterReuter/workshop-raspberrypi-64bit-os)
* [Compute Module Product Page](https://www.raspberrypi.org/products/compute-module-3-plus/)
