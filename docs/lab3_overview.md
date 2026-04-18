# Lab 3 Overview: Performance Comparison of Routing Methods

## Lab Goal
You will compare three routing approaches in a small simulated network: Static Routing, RIP v2, and OSPF (area 0).
You will evaluate them in terms of: convergence time, packet delivery (packet loss), and network efficiency.

---

## Core Routing Concepts

### What routing is
- Routers forward packets between different IP networks using a routing table.
- Each PC on a LAN uses a default gateway (the router) to reach other networks.

### Static vs dynamic routing
**Static routing**
- Routes are manually configured by the administrator.
- Simple, predictable, and uses very little CPU or bandwidth.
- Does not automatically reroute if a link fails.

**Dynamic routing**
- Routers run a routing protocol (e.g., RIP, OSPF) to exchange routing information.
- Routes are automatically updated when the network topology changes.
- Adapts to failures and growth.

---

## RIP vs OSPF Basics

### RIP (Routing Information Protocol v2)
- Type: Distance-vector routing protocol.
- Metric: Hop count.
- Maximum 15 hops; limited scalability.
- Slow convergence.

### OSPF (Open Shortest Path First)
- Type: Link-state routing protocol.
- Metric: Cost (bandwidth).
- Designed for large, complex networks.
- Fast convergence.

---

## Lab 3 Tasks

### Topology and setup (Part A)
- Build a topology with 4 routers.
- Assign IP addresses to router interfaces and LAN PCs.

### Static routing (Part B)
- Configure static routes on all routers.
- Test full connectivity (ping).
- Record behavior when a link fails.

### RIP configuration (Part C)
- Configure RIP version 2.
- Measure convergence time and packet loss after link failure.

### OSPF configuration (Part D)
- Configure OSPF (area 0).
- Measure convergence time and routing efficiency.

### Failure simulation (Part E)
- Shut down one link and observe recovery.

### Analysis report (Part F)
- Compare Static, RIP, and OSPF.
- Present results in a table.
