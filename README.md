# dhcp-client-register-dns
Small script to automatically register a hosts hostname in DNS servers.

ISC dhclient-post-exit hook script to use nsupdate to register the
hostname and the reverse entries in DNS with the system DNS servers 
(usually set by the same DHCP server.

This script uses nsupdate, and as such with the correct 
authentication keys can do secure DNS.

### Dependencies!

* sipcalc: Used to reverse the IPv6 address. 
* nsupdate: Used to do the DNS updates. Duh.

### Installation
This script should be installed as a dhclient post-exit script
Usually this would be putting this file in 

   /etc/dhcp/dhclient-exit-hooks.d/register-dns

and not forgetting to chmod a+x it.

### Configuration
Not much
