# Preparing a Virtual Machine for BlissOS

## Introduction

Bliss OS supports many hypervisors and virtual machine monitors. Each Virtual machine utility will have it's own configurations that are available, However they all generally share the same general set of features to choose from.

## Supported Virtual Machine Software

BlissOS supports almost every major virtual machine utility that is out there. Below is a small list of ones that you can expect to find support for, but this is in no way exhaustive.

* Qemu based machines (Proxmox, Libvirt, Unraid)
* VirtualBox
* CrosVM
* Hyper-V
* Vmware
* XCP-NG
* XenServer

Most VMMs will support Bliss OS as BlissOS is intended to be as generic is possible, Support for some features however may be missing, Things like Accelerated graphics can often be supported on a case by case basis, with the best support being Virtio graphics.

## Setting up a Virtual Machine

When it comes to configuring the virtual machine, there is tons of flexibility, very little configuration values are a hard requirement, so we will go over the general minimums.

A properly configured virtual machine should expose;

* A minimum of 1gb of ram
* A CPU newer then an intel core series 2xxx or an AMD FX series CPU.
* A virtual machine should expose a VGA capable display
* For acceleration, BlissOS uses Mesa, Though not every GPU supported by android, Both VMWare's vGPU and Virtio GPU are supported for hardware acceleration. Currently limited to opengl for emulated gpu support, Pass through a physical GPU for vulkan support.
* Bliss supports a large number of emulated/virtualized inputs and can even multi touch with the right configuration, this largely relies on support for upstream projects. An example of this is multitouch when supported under Qemu with GTK backend. Gamepads, Tablets, etc, should all work if they use the appropriate generic APIs.
* BlissOS does not currently support most integration features of virtual machine utilities. 

## Install BlissOS

When it comes to installing the virtual machine, most steps will remain the same as a physical machine, to avoid rehashing that, Please refer to the main installation page, and only view the below as exceptions to said page.