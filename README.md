# gcp-magic
Quickly allow modification to GCP firewall rules.

This is a simple bash script to allow a person to add and remove a firewall rule in GCP by just specifying a port number.

I developed this were the firewall rules are very tight, but I occassionally needed to open a port for a few minutes, and then shut it back down.

## Usage:
```magic list | open <port_number> | close <port_number>```

## Examples
```
$ magic open 3389    # opens up port 3389 for RDP
$ magic open 22      # opens up port 22 for SSH
$ magic close 3389   # close (remove) port 3389
$ magic close 22     # close (remove)  port 3389
$ magic list         # list out the current 
```
