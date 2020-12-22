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

## architectural requirements

### single-host deployment
- all services should be configured to listen on the loopback ip address
- your shared network storage mountpoint should just be a directory with some filesystem space available

### distributed deployment
- one or more network storage servers
- one or more compute servers
- a mysql database server
- an nginx webserver running vmapi

### vmlab client dependencies
- ruby >= 2.6.6
- tiger vncviewer (or another vncviewer supporting x509/TLS)
- ssh
- git
- pass
- gnupg
- openssl
- bash

### compute server dependencies
- linux kernel with kvm support or modules
- openvswitch
- qemu-kvm
- ssh
- ability to mount your shared network storage

### storage server dependencies
- ability to export some kind of shared network storage

### database server dependencies
- mysql database server

### web server dependencies
- nginx
- vmapi (this is vmlab's backend web application stack implementing a cloud management rest api)
