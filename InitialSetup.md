# Initial setup kubernetes with PI's

## Introduction 

This document describe the initial steps that you need to take.

## Requirements

- PI (2/3)
- SSD with minimal of 8gb
- Router with internet routable gateway

## Software

- Etcher (Used to burn an image into the ssd)
- Raspian Stretch lite

## First steps

Please prepare an ssd with raspian stretch lite and put an empty file in the root named ssh. This makes sure that we can access the pi over ssh.

[Headless SSH](https://www.raspberrypi.org/documentation/remote-access/ssh/)

Now connect it to a router, locate the ip adress and ssh into the pi.

Also make sure to change the default password.

[Change password](https://www.raspberrypi.org/documentation/configuration/security.md)

Now the PI's are ready for hacking.