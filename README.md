📘 NETWORK DESIGN REPORT: CAPE VERDE ↔ GHANA TOPOLOGY
1. IP Addressing Scheme (CIDR)
LAN 1 (Ghana):
Network: 192.168.10.0/29
Subnet Mask: 255.255.255.248
Usable IPs: 192.168.10.1 – 192.168.10.6
Broadcast: 192.168.10.7
Router IP: 192.168.10.1
LAN 2 (Cape Verde):
Network: 172.16.1.0/29
Subnet Mask: 255.255.255.248
Usable IPs: 172.16.1.1 – 172.16.1.6
Broadcast: 172.16.1.7
Router IP: 172.16.1.1
WAN Link (Between Routers):
Network: 10.1.1.0/30
Subnet Mask: 255.255.255.252
Usable IPs: 10.1.1.1 (Ghana), 10.1.1.2 (Cape verde)
Broadcast: 10.1.1.3

2. Device Configuration Summary
Each router (Cape Verde and Ghana) connects to:
One local LAN via GigabitEthernet.
One WAN connection via Serial interface.
Each LAN includes:
4 PCs
1 Server
All devices statically assigned IPs within subnet range.

3. Access Control List (ACL) Summary
Objective: Secure WAN traffic by allowing only essential protocols.
Rules Applied on Serial Interfaces:
Permit ICMP (ping) for testing/diagnostics.
Permit TCP port 80 (HTTP) for web services.
Deny all other IP traffic.

4. Summary
Efficient subnetting using /29 (6 usable IPs per LAN).
Point-to-point WAN uses /30 (2 usable IPs).
ACL restricts unnecessary traffic, improving network security.
Design supports basic inter-router communication, secure LAN operation, and controlled WAN access.
