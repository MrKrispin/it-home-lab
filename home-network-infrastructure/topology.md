# Network Topology

## 1. Overview

This document describes the physical and logical layout of the residential network, including network infrastructure, device connections, and IP addressing.

## 2. Physical Network Topology

### Infrastructure Devices

| Device | Model | Function |
|---|---|---|
| Gateway | AT&T Gateway | Internet access, routing, and DHCP |
| Managed Switch | TP-Link SG2008P | Ethernet switching and network management |
| Wireless Access Point | TP-Link EAP723 | Wireless connectivity |

### Physical Connections

- The AT&T gateway connects to the managed switch.
- The managed switch connects to the hallway-mounted wireless access point and is powered using the switch's PoE capability
- Cat6 Ethernet runs provide wired connectivity to multiple rooms.

### Network Diagram

*Physical network diagram to be added after verifying all connections and switch ports.*

## 3. Logical Network Topology

The existing network uses the AT&T gateway for routing and DHCP services.

The managed switch and wireless access point provide local network connectivity to all devices

*Detailed IP addressing, VLAN configurations, and network segmentation will be documented after verification.*

## 4. Planned Updates

- [ ] Document switch port assignments.
- [ ] Create a simplified physical network diagram.
- [ ] Record the LAN subnet and gateway address.
- [ ] Document DHCP reservations and VLANs as configured.
