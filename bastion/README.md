# Bastion

The bastion host is supposed to be a hardened internal machine to allow for SSH jumps and internal connection to the other machines within the network.

Based on the requirements for the network this machine requires the following capabilities.

1. SSH server to allow for SSH jumping to internal machines
1. Web browser available via X11-Forwarding SSH to access the pfSense control panel without exposing it externally