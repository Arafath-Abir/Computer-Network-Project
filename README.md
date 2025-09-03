# Computer Network Project

This repository contains two Cisco Packet Tracer projects that demonstrate core concepts in computer networking. These projects were developed as part of academic learning and practice with network design, configuration, and routing protocols.

---

## 📂 Projects Included

### 1. **com Network 1.pkt**
- Focuses on **OSPF (Open Shortest Path First) Routing Protocol**.  
- Demonstrates how OSPF dynamically updates routing tables in a multi-router environment.  
- Includes subnetting, router configurations, and verification using simulation mode.  
- Useful for understanding link-state routing and efficient path selection.

### 2. **Com Network 2.pkt**
- A **basic computer network topology** project.  
- Includes switches, routers, PCs, and servers connected in a structured design.  
- Configures IP addressing and tests connectivity with `ping` and other tools.  
- Serves as a foundation for beginners to understand LAN/WAN design in Packet Tracer.

---

## 🔧 Tools & Technologies
- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)  
- OSPF (Routing Protocol)  
- IP Addressing & Subnetting  
- Network Simulation & Troubleshooting  

---

## 🎯 Learning Outcomes
- Designing and simulating computer networks in Packet Tracer.  
- Configuring routing protocols (OSPF).  
- Practicing subnetting and IP planning.  
- Testing and troubleshooting connectivity in simulated environments.  

---

## 📊 Topology Diagrams

### 1) `Com Network 1` — OSPF multi-router lab

```text
           ┌──────────┐        OSPF Area 0        ┌──────────┐
   LAN-A   │  PC-A    │                           │  PC-B    │   LAN-B
   10.0.1.10/24       │                           │          │   10.0.2.10/24
           └────┬─────┘                           └────┬─────┘
                │                                       │
           ┌────┴────┐       ┌──────────┐        ┌──────┴─────┐
           │ SW-A    │-------│  R1      │--------│   SW-B     │
           └────┬────┘  G0/0 │(ABR)     │ G0/1   └────┬───────┘
                │            └────┬─────┘               │
                │                 │                      │
           10.0.1.0/24       Area 0 (Backbone)      10.0.2.0/24
                               │
                               │
                          ┌────┴─────┐
                          │   R2     │  Area 1
                          └────┬─────┘
                               │
                          ┌────┴─────┐
                          │  SW-C    │
                          └────┬─────┘
                               │
                          ┌────┴─────┐
                          │  Server  │  10.0.3.20/24
                          └──────────┘



### 2) `Com Network 1` — OSPF multi-router lab

 PC1 10.1.1.10/24            PC2 10.1.1.11/24
     │                            │
     │                            │
   ┌─┴───┐                    ┌───┴─┐
   │ SW1 │--------------------│ SW2 │
   └─┬───┘        Trunk/      └───┬─┘
     │           Access Links      │
     │                              │
   ┌─┴───────────────┐         ┌────┴──────────────┐
   │   Router (R)    │---------│     Server        │
   │ G0/0: 10.1.1.1  │         │ 10.1.2.20/24      │
   │ G0/1: 10.1.2.1  │         └───────────────────┘
   └─────────────────┘
