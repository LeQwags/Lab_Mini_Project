Here’s a cleaned-up Markdown version you can drop into a `.md` file, with inline references and a short reference list at the end.

---

# Lab 3 & Mini‑Project Overview

This document summarizes the key concepts and tasks you should understand before implementing your Lab 3 and the Campus Network mini‑project.file+1

---

## Lab 3: Performance Comparison of Routing Methods

## Lab goal

You will compare three routing approaches in a small simulated network: Static Routing, RIP v2, and OSPF (area 0).ioriver+1  
You will evaluate them in terms of: convergence time, packet delivery (packet loss), and network efficiency.geeksforgeeks+2

---

## Core Routing Concepts

## What routing is

- Routers forward packets between different IP networks using a routing table (list of destination networks and next hops).[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    
- Each PC on a LAN uses a default gateway (the router) to reach other networks.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    

## Static vs dynamic routing

**Static routing**

- Routes are manually configured by the administrator.ioriver+1
    
- Routes do not change unless you edit them.geeksforgeeks+1
    
- Simple, predictable, and uses very little CPU or bandwidth.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- Does not automatically reroute if a link fails.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- Best for small, stable networks.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    

**Dynamic routing**

- Routers run a routing protocol (e.g., RIP, OSPF) to exchange routing information.ioriver+1
    
- Routes are automatically updated when the network topology changes.ioriver+1
    
- Uses more CPU and bandwidth but adapts to failures and growth.ruijie+1
    
- Better for larger or changing networks.ioriver+1
    

In this lab you are explicitly asked to understand the trade‑offs between static and dynamic routing.[file](file:///C:/Users/tl/Downloads/Lab%20and%20Mini_Project_%20Apr%202026.pdf)

---

## RIP vs OSPF Basics

## RIP (Routing Information Protocol v2)

- Type: Distance‑vector routing protocol.tutorialspoint+1
    
- Metric: Hop count (number of routers to reach a destination).atlas+1
    
- Maximum 15 hops; limited scalability.tutorialspoint+1
    
- Uses periodic updates (e.g., every 30 seconds) and converges relatively slowly.atlas+1
    
- Configuration is simple; suited for small networks.tutorialspoint+1
    

In your lab you will:

- Enable RIP v2 on all routers and advertise all connected networks.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Measure convergence time and packet loss after a link failure.geeksforgeeks+1
    

## OSPF (Open Shortest Path First)

- Type: Link‑state routing protocol.atlas+1
    
- Metric: Cost, typically based on bandwidth.tutorialspoint+1
    
- No fixed hop‑limit; designed for large, complex networks.[tutorialspoint](https://www.tutorialspoint.com/article/difference-between-rip-and-ospf)
    
- Uses triggered updates and converges much faster than RIP.atlas+1
    
- More complex to configure but more efficient and scalable.[tutorialspoint](https://www.tutorialspoint.com/article/difference-between-rip-and-ospf)
    

In your lab you will:

- Configure OSPF in area 0 on all routers.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Measure convergence time and “routing efficiency” (e.g., how direct routes are, overhead, etc.).atlas+2
    

---

## Lab 3 Tasks (What You Actually Do)

## Topology and setup (Part A)

- Build a topology with 4 routers, each connected to its own LAN, using an interconnected mesh or ring.file+1
    
- Use Cisco Modeling Labs (CML) or another simulator and mention which tool you used.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Assign IP addresses to:
    
    - Router interfaces.
        
    - LAN PCs.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
        

## Static routing (Part B)

- Configure static routes on all routers so every LAN can reach every other LAN.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Test full connectivity by pinging between all PCs.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Record:
    
    - Time taken to configure all static routes.
        
    - Behaviour when a link fails (some destinations will become unreachable until routes are manually fixed).geeksforgeeks+1
        

## RIP configuration (Part C)

- Configure RIP version 2 and advertise all networks.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- After causing a link failure, measure:
    
    - Convergence time (how long until routing stabilizes).
        
    - Packet loss during the failure and convergence.atlas+2
        

## OSPF configuration (Part D)

- Configure OSPF (area 0) on all routers.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Measure:
    
    - Convergence time.
        
    - Routing efficiency (e.g., quality of chosen paths, protocol overhead).tutorialspoint+2
        

## Failure simulation (Part E)

- Shut down one link (for example, between R1 and R2).[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- Observe and note:
    
    - Network recovery time (convergence).
        
    - Packet loss.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
        

## Analysis report (Part F)

- Compare Static, RIP, and OSPF based on your measurements and observations.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- Present results in a table showing convergence time, packet loss, and efficiency for each method.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- Recommend the best protocol for this topology, with justification (usually OSPF for speed and scalability, static for simplicity in very small networks).atlas+2
    

---

## What You Should Understand Conceptually

Before configuring, make sure you understand:

- How routers use routing tables to forward packets between networks.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    
- Why static routes are simple but do not recover automatically from failures.geeksforgeeks+1
    
- Why dynamic protocols (RIP, OSPF) can automatically reroute traffic when links fail.geeksforgeeks+1
    
- Key differences between RIP and OSPF:
    
    - RIP: hop‑count metric, slow convergence, limited to small networks.tutorialspoint+1
        
    - OSPF: cost metric, fast convergence, scales to large networks.atlas+1
        
- What “convergence time”, “packet loss”, and “network efficiency” mean in practical terms for your experiments.file+4
    

---

## Mini‑Research Project: Campus Network

The mini‑project applies the same routing ideas to a larger, more realistic enterprise network for a university annex building.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)

## Project goal

Design and simulate a reliable, scalable, and secure campus network for:[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)

- 3 departments (Engineering, ICT, Administration).
    
- 2 computer labs.
    
- 1 server room.
    
- Wireless access for students.
    

You must use CML or another simulator and mention which one you used.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)

---

## Mini‑Project Tasks and Concepts

## Network design (Part A)

- Propose an overall topology, typically star or hierarchical (Core–Distribution–Access).[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    
- Draw a clear network diagram.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    

## IP addressing (Part B)

- Allocate IP subnets for:
    
    - Each department.
        
    - Each lab (if separate).
        
    - Servers.
        
    - Wireless users.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
        
- Use subnetting or VLSM so that each subnet size matches its host requirements.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    

## VLAN design (Part C)

- Create VLANs such as:[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    
    - VLAN 10: Engineering.
        
    - VLAN 20: ICT.
        
    - VLAN 30: Admin.
        
    - VLAN 40: Students WiFi.
        
    - VLAN 50: Servers.
        

You should understand that VLANs separate broadcast domains and logically group users on switches.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)

## Routing (Part D)

- Configure inter‑VLAN routing (either via a router‑on‑a‑stick or a Layer 3 switch).[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    
- Use either OSPF or static routing for routing between VLANs/subnets.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)[tutorialspoint](https://www.tutorialspoint.com/article/difference-between-rip-and-ospf)
    

## Services (Part E)

- Implement key network services:[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    
    - DHCP for dynamic IP address assignment to hosts.
        
    - DNS (optional) for name resolution.
        
    - Default gateway settings for each VLAN/subnet.
        

## Security with ACLs (Part F)

- Use Access Control Lists to:[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    
    - Block student (WiFi) VLAN access to the Admin network.
        
    - Still allow students to access servers (e.g., web or application servers).
        

This requires you to know where to apply ACLs (which interface, inbound or outbound) and how to write basic permit/deny statements.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)

## Testing (Part G)

- Verify:[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    
    - End‑to‑end connectivity between allowed networks.
        
    - VLAN isolation (blocked communication where it should be blocked).
        
    - Internet access (optional, since this is a simulated environment).
        

## Final report (Part H)

Your report must include:[indeed](https://www.indeed.com/career-advice/career-development/dynamic-routing-vs-static-routing)

- Network diagram.
    
- IP addressing plan.
    
- Configuration summary (high‑level explanation, not full configs).
    
- Justification of design decisions (why that topology, routing method, VLAN structure, ACL rules, etc.).
    

---

## Practical Skills You Should Be Ready With

To actually complete both the lab and the mini‑project you should be comfortable with:

- Designing small IP addressing schemes and subnets.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Creating basic topologies in Cisco Modeling Labs or similar tools.developer.cisco+2
    
- Assigning IP addresses to router interfaces and PCs in the simulator.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- Configuring:
    
    - Static routes.geeksforgeeks+1
        
    - RIP v2.atlas+1
        
    - OSPF area 0.tutorialspoint+1
        
- Inter‑VLAN routing, VLAN creation, DHCP, and simple ACLs.[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)
    

---

## References

- Lab and Mini‑Project brief: “Lab and Mini_Project_ Apr 2026.pdf”.indeed+2[youtube](https://www.youtube.com/watch?v=FEdhERayt-U)ioriver+1
    
- GeeksforGeeks – “Static and Dynamic Routing”.[geeksforgeeks](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
    
- IO River – “Static vs Dynamic Routing: What’s The Difference”.[ioriver](https://www.ioriver.io/blog/static-dynamic-routing)
    
- TechTarget – “Static Vs. Dynamic Routing: What is the Difference?”.[techtarget](https://www.techtarget.com/searchnetworking/answer/Static-and-dynamic-routing)
    
- TutorialsPoint – “Difference between RIP and OSPF”.[tutorialspoint](https://www.tutorialspoint.com/article/difference-between-rip-and-ospf)
    
- Cisco Developer – “Cisco Modeling Labs v2.9: Getting Started / Initial Setup”.developer.cisco+1
    
- Atlas / other Q&A – summaries comparing RIP and OSPF metrics and convergence.[atlas](https://www.atlas.org/solution/55c4aa79-4b32-4784-9c63-be79b5706a16/compare-rip-and-ospf-routing-algorithms-on-the-following-aspects-algorithm-type-metric-convergence-time-and-scalability)
    
- Ruijie / other vendor docs – “Dynamic Route vs Static Route: Definitions, Pros and Cons”.[ruijie](https://www.ruijie.com/en-global/support/faq/dynamic-route-vs-static-route)
    

---

You can save everything between the `---` lines as `lab3_mini_project_overview.md`. If you want, I can also help you create a second `.md` just for your final lab report structure (with tables ready to fill in).