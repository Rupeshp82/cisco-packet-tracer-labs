Lab 01 — Static Routing Between Two LANs

##Objective

Build a small network using two routers and configure static routing to allow communication between two separate LANs.

## Topology

PC1 - Switch1 - R1 - R2 - Switch2 - PC2

## IP Addressing

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
|---|---|---|---|---|
| PC1 | NIC | 192.168.10.10 | 255.255.255.0 | 192.168.10.1 |
| R1 | G0/0 | 192.168.10.1 | 255.255.255.0 | — |
| R1 | G0/1 | 10.0.0.1 | 255.255.255.252 | — |
| R2 | G0/0 | 10.0.0.2 | 255.255.255.252 | — |
| R2 | G0/1 | 192.168.20.1 | 255.255.255.0 | — |
| PC2 | NIC | 192.168.20.10 | 255.255.255.0 | 192.168.20.1 |

## Static Routes

### R1

```text
ip route 192.168.20.0 255.255.255.0 10.0.0.2

### R2

```text
ip route 192.168.10.0 255.255.255.0 10.0.0.1

