# Homelab Network Architecture

The goal of the homelab is to allow easy spin up of VM's and testing of different software across a range of hosts.

This homelab will be virtualized on my gaming PC without an external need for a router to keep control within the one enivronment with no public availability.
The homelab will only be accessible through one pfSense firewall box which will process incoming requests via a NAT network and direct it to the correct VM or internal homelab host.

Currently the structure goes:
```
Host PC
    |               NAT Network type with ports 22,80,443
pfSense VM
    |               Internal Virtualbox network
-------------
|           |
bastion     esxi
```

## Bastion Host
The Bastion host is supposed to be a dedicated PC within the network to allow for bridged connections to the other internal devices without exposing them to the public internet.

In the case of this system we are using the bastion host as the dedicated SSH box to allow for jumping into each machine within the esxi host.

This host should be hardened and not allow any unauthorized users within.