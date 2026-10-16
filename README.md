# CCNA Enterprise Network Capstone

A Cisco Packet Tracer enterprise network featuring HQ and branch connectivity, VLAN segmentation, centralized services, internet access, and security controls.

## Topology
- HQ: Engineering, IT, Admin, Server, and Guest VLANs
- Branch: Departmental VLANs and Guest VLAN
- ISP: Routes traffic between HQ, Branch, and an external network
- External server: Hosts `internet.com`

## Key Technologies
- VLANs and router-on-a-stick inter-VLAN routing
- OSPF dynamic routing
- DHCP and DHCP relay
- DNS for internal and external hostnames
- NAT/PAT for internet access
- Extended ACLs for Guest network isolation
- SSH, port security, PortFast, BPDU Guard, and DHCP Snooping

## Key Addressing
| Network | Subnet |
|---|---|
| HQ Engineering | `10.1.10.0/24` |
| HQ IT | `10.1.20.0/24` |
| HQ Admin | `10.1.30.0/24` |
| HQ Servers | `10.1.40.0/24` |
| HQ Guest | `10.1.50.0/24` |
| Branch Engineering | `10.2.10.0/24` |
| Branch IT | `10.2.20.0/24` |
| Branch Admin | `10.2.30.0/24` |
| Branch Guest | `10.2.50.0/24` |
| HQ–ISP link | `10.11.10.0/24` |
| Branch–ISP link | `10.12.10.0/24` |
| External server | `198.51.100.2` |

## Services & Security
- Internal application server: `10.1.40.2` (`company.com`)
- Infrastructure/DNS server: `10.1.40.3`
- ISP-based PAT for HQ and Branch clients
- Guest ACL restricts access to the internal application server while permitting intended internet access
- Switch hardening: edge-port protections, unused-port shutdown, port security, and DHCP Snooping
- SSH for device management

## Validation
Core routing, DHCP/DNS, website access, PAT, and Guest ACL behavior were tested in Packet Tracer.

> Simulation project using documentation-only external IP ranges.

Add your saved `.pkt` file to the repository.
