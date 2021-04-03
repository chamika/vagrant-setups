# multi-node-k8s-cluster

Multi-node kubernetes cluster with 1 leader(master) node and 2 worker nodes running on 3 Ubuntu 18.04 Vagrant virtual machines.

This is based on the tutorial  "[Kubernetes Setup Using Ansible and Vagrant](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/)". However, minor changes are done to work with more updated versions.

## Prerequisites
- Vagrant should be installed on your machine along with working Vagrant provider like Oracle VirtualBox
- Ansible should be installed on you machine.

## Environment
- 1 leader node (Running Ubuntu 18.04) - kubeadm as Kubernetes runtime.
- 2 worker nodes (Running Ubuntu 18.04)

## Usage

### Start the cluster

```shell
vagrant up
```

### SSH into leader node

```shell
vagrant ssh k8s-master
```

Once you SSH into the master node you can use `kubectl` to deploy or make any changes to the cluster

### Suspend the cluster

```shell
vagrant suspend
```

To start the cluster again run 

```shell
vagrant up
```

### Delete the cluster

```shell
vagrant destroy
```