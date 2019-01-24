# Network-Lab - Infrastructure as Code Demo

## Topology

* HQ:
  * hq-wan-mpls: csr-1000v (mpls DMVPN hub)
  * hq-wan-inet: csr-1000v (inet DMVPN hub)
  * hq-mc: csr-1000v (pfr master controller - IOS CA root)
  * hq-core: IOSv
  * hq-dc-core-1/2: NX-OSv
* Branch1 (L3 site):
  * branch1-wanc: csr-1000v (wan edge - dual-transport inet+mpls)
  * branch1-core: IOSvL2 (LAN Core L3 enable)
* Branch2 (L2 Site):
  * branch2-wan: csr-1000v (wan edge - dual-transport inet+mpls)
  * branch2-lan: IOSvL2 (LAN acces L2 only)
* MPLS/INET Backbone
  * Provider: IOSv (provides simulation of MPLS and Internet providers using vrf-lite)
  
## Network Logical Topology

![Alt text](documentation/diagrams/logical_network_topology.jpg?raw=true "Logical Network Topology")

## Network Physical Topology (VIRL)

![Alt text](documentation/diagrams/physical_network_topology.jpg?raw=true "Physical Network Topology")
