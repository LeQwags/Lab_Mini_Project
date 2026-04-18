# VLAN Basics and Inter-VLAN Routing

VLANs (Virtual Local Area Networks) are essential for segmenting large campus networks like the one in the mini-project.

## VLAN Concepts
- **Segmentation**: VLANs logically separate a physical switch into multiple virtual switches, isolating broadcast domains.
- **Security**: By placing different departments (e.g., Admin vs. Students) on different VLANs, you can control traffic flow between them.
- **Mini-Project Application**:
  - VLAN 10: Engineering
  - VLAN 20: ICT
  - VLAN 30: Admin
  - VLAN 40: Students WiFi
  - VLAN 50: Servers

## Inter-VLAN Routing
Since VLANs are isolated, a router or Layer 3 switch is required to move traffic between them.
- **Router-on-a-stick**: A single physical interface on a router is divided into sub-interfaces, each acting as a default gateway for a specific VLAN.
- **Layer 3 Switching**: Using SVIs (Switch Virtual Interfaces) on a multilayer switch for faster routing.

## References
- [TutorialsPoint – VLANs in Computer Networks](https://www.tutorialspoint.com/vlan-in-computer-network)
- [Cisco – Inter-VLAN Routing Configuration](https://www.cisco.com/c/en/us/support/docs/lan-switching/inter-vlan-routing/10023-3.html)
- [Cisco – DHCP Configuration Guide](https://www.cisco.com/c/en/us/support/docs/ip/dynamic-host-configuration-protocol-dhcp/9609-3.html)
