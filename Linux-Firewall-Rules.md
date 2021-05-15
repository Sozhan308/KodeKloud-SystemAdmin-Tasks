# *Linux Firewalld Rules*

## Description

### The Nautilus system admins team recently deployed a web UI application for their backup utility running on the Nautilus backup server in Stratos Datacenter

### The application is running on port 6000. They have firewalld installed on that server. The requirements that have come up include the following

### Open all incoming connection on 6000/tcp port. Zone should be public


_Solution - adding port_

**List all allowed ports**

`firewall-cmd --list-ports`

### Add a port to the allowed ports to open it for incoming traffic 

`firewall-cmd --add-port=port-number/port-type`

`firewall-cmd --add-port=6000/tcp`

The port types are either tcp, udp, sctp, or dccp. The type must match the type of network communication.

Make the new settings persistent:

`firewall-cmd --runtime-to-permanent`
The port types are either tcp, udp, sctp, or dccp. The type must match the type of network communication.

`systemctl reload firewalld`

-----------------------------------

_Solution -  Remove port_

**List all allowed ports**

`firewall-cmd --list-ports`

**_WARNING_**

This command will only give you a list of ports that have been opened as ports. You will not be able to see any open ports that have been opened as a service. Therefore, you should consider using the --list-all option instead of --list-ports.

### Remove the port from the allowed ports to close it for the incoming traffic

`firewall-cmd --remove-port=port-number/port-type`

### Make the new settings persistent:

`firewall-cmd --runtime-to-permanent`
