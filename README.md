# Vagrant_K8s
Sets up a single node cluster or a multi-node cluster

## Single-node cluster
VAGRANT_VAGRANTFILE=Vagrantfile.single-node vagrant up

VAGRANT_VAGRANTFILE=Vagrantfile.single-node vagrant destroy

## Multi-node cluster
## Changes1: node require the docker driver to change to required systemd, introduced a script configure-systemd.sh
## Changes2: update the ubuntu image version to 18.04
## Changes3: Changes virtualization provider to KVM provider (libvirt)
## Changes4: Made minor fixes to copy the join command std out to local
## Known Error: At this  moment the script need to be run twice because the join command is not getting produced before worker nodes looking for it , which is making the script to fail at first time
VAGRANT_VAGRANTFILE=Vagrantfile.multi-node vagrant up

VAGRANT_VAGRANTFILE=Vagrantfile.multi-node vagrant destroy



