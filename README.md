# vmlab

## overview
vmlab is a command-line console interface for managing virtual machines.

currently, only the qemu-kvm hypervisor on linux x86_64 and x86 is supported.

it can be deployed as a distributed cluster or you can run it on a single machine such as a laptop.

## roadmap
support for linux qemu-kvm hypervisor on arm architecture

freebsd bhyve hypervisor support

openbsd vmm hypervisor support

postgresql rdbms support

## setup



### dependencies
- ruby >= 2.6.6
- qemu-kvm
- openvswitch
- tiger vncviewer (or another vncviewer supporting x509/TLS)
- ssh
- git
- pass
- gnupg
- openssl
- bash

##### mandatory
- one or more network storage servers
- one or mor compute servers (aka hosts) with qemu-kvm installed
- a mysql database server
##### optional
- a webserver to expose the rest api
- 
