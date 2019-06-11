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

setup network and change hostname 

`raspi-config`

change dhcp

```
interface eth0
static ip_address=x.x.x.y/24
static routers=x.x.x.1
static domain_name_servers=8.8.8.8
```


Now the PI's are ready for hacking.

## Kubernetes

Commands are not shown here just general steps. And should be done on all nodes

1. Get and install docker always look at the script.
2. Disable swap
3. Add cgroup config to boot.
4. Add kube to debian package manager and add key,
5. Install kubeadm

## Master node

1. Pre pull images
2. Init kubeadm with a token ttl of 0
3. get kubeconfig and install you can also use this to connect to your cluster
4. Note the join token
5. Install weavenet

## Worker nodes

1. Join nodes to cluster

## Test

- kubectl create deployment nginx --image=nginx
- kubectl create service nodeport nginx --tcp=80:80

## Extra

- copy kubeconfig to local and run kubectl

## Tips

use devmgmt.msc for flash 

[Kube-pi](https://medium.com/nycdev/k8s-on-pi-9cc14843d43)

[KubeARM](https://blog.hypriot.com/post/setup-kubernetes-raspberry-pi-cluster/)
