# Lab23-LAN-3-Niveaux-VLAN-HSRP-EtherChannel-Routage-OSPF-NAT-dynamique
This repository presents a comprehensive three-tier enterprise network lab designed to demonstrate redundancy, scalability, and dynamic internet access using Cisco technologies.

The architecture is built around access (L2), distribution/core (L3), and edge routing layers. Multiple Layer 2 access switches host end devices across two VLANs (VLAN 10 – IT, VLAN 20 – HR). These VLANs are trunked to redundant Layer 3 core switches, where inter-VLAN routing and first-hop redundancy are implemented using HSRP.

Key technologies and concepts implemented in this lab include:

VLAN segmentation (IT and HR)

HSRP to provide gateway redundancy for each VLAN using virtual IP addresses

DHCP services on Layer 3 switches for automatic IP assignment

EtherChannel (PAgP) between core switches to increase bandwidth and provide link redundancy

OSPF dynamic routing across all Layer 3 devices for full network reachability

Dynamic NAT with PAT on the edge router to allow internal users to access the Internet using a public address pool

Default route propagation via OSPF from the edge router to the internal network

All PCs use the HSRP virtual IP address as their default gateway, ensuring uninterrupted connectivity even if one Layer 3 switch or VLAN interface fails.

Outcome:

End devices in VLAN 10 and VLAN 20 can communicate internally and access the Internet.

Gateway redundancy is guaranteed through HSRP.

Link-level redundancy and load sharing are achieved with EtherChannel.

Routing is fully dynamic using OSPF.

Internet access is securely enabled via Dynamic NAT and PAT.

This lab is ideal for practicing enterprise network design, high availability, and routing/NAT integration in a realistic multi-layer Cisco environment.
