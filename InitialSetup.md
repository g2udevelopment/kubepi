# Initial setup kubernetes with PI's

## Introduction 

This document describe the initial steps that you need to take to setup the pi.

## Requirements

- PI (2/3)
- SD with minimal of 8gb
- Router with internet routable gateway

## Software

- Etcher (Used to burn an image into the sd)
- Raspian Stretch lite

## First steps

Please prepare an sd with raspian stretch lite and put an empty file in the root named ssh. This makes sure that we can access the pi over ssh.

[Headless SSH](https://www.raspberrypi.org/documentation/remote-access/ssh/)

Now connect it to a router, locate the ip adress and ssh into the pi.

Also make sure to change the default password. `passwd`

[Change password](https://www.raspberrypi.org/documentation/configuration/security.md)

setup network

`raspi-config`

change dhcp



Now the PI's are ready for hacking.

## Tips

use devmgmt.msc for flash 

[Kube-pi](https://medium.com/nycdev/k8s-on-pi-9cc14843d43)
