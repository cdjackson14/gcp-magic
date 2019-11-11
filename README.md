# gcp-magic
Quickly allow modification to GCP firewall rules.

This is a simple bash script to allow a person to add and remove a firewall rule in GCP by just specifying a port number.

I developed this were the firewall rules are very tight, but I occassionally needed to open a port for a few minutes, and then shut it back down.

## Usage:
```magic list | open <port_number> | close <port_number>```

This will create a firewall rule that starts with cdj-tmp- and adds the port number.

```
$ magic open 22
Creating firewall...⠶Created [./project/global/firewalls/cdj-tmp-22].
Creating firewall...done.
NAME        NETWORK  DIRECTION  PRIORITY  ALLOW   DENY  DISABLED
cdj-tmp-22  default  INGRESS    1000      tcp:22        False
```

## Examples
```
$ magic open 3389    # opens up port 3389 for RDP
$ magic open 22      # opens up port 22 for SSH
$ magic close 3389   # close (remove) port 3389
$ magic close 22     # close (remove)  port 3389
$ magic list         # list out the current 
```
