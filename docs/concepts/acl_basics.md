# Access Control Lists (ACLs)

ACLs are the primary tool for implementing security policy in the campus network mini-project.

## Purpose
ACLs allow you to permit or deny traffic based on criteria such as source/destination IP addresses, protocols, and port numbers.

## Mini-Project Requirements
- **Restriction**: Block the Student WiFi VLAN from accessing the Admin network.
- **Permit**: Allow Students to access specific servers (e.g., Web or Application servers) in the Server VLAN.

## Best Practices
- **Standard ACLs**: Used to filter based on source IP only.
- **Extended ACLs**: Used to filter based on source/destination IP, protocol (TCP/UDP), and port numbers (HTTP, DNS, etc.).
- **Placement**: Apply ACLs as close to the source of the traffic as possible for extended ACLs, and close to the destination for standard ACLs.

## References
- [Cisco – Configuring Network Security with ACLs](https://www.cisco.com/c/en/us/support/docs/security/ios-firewall/23602-confaccesslists.html)
