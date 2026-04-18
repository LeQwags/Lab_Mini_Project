# OSPF (Open Shortest Path First)

OSPF is a widely used link-state routing protocol designed for scalability and speed.

## Key Features
- **Algorithm**: Link-state (Dijkstra's Shortest Path First).
- **Metric**: Cost, which is typically based on the bandwidth of the link.
- **Scalability**: No fixed hop-limit; supports hierarchical designs using areas.
- **Updates**: Uses triggered updates (sends info only when a change occurs), leading to faster convergence.
- **Complexity**: More complex to configure and requires more router resources than RIP.

## Usage in Lab 3
In this lab, you will configure OSPF in **Area 0** (the backbone area) to evaluate:
- **Routing Efficiency**: How direct the chosen paths are.
- **Recovery Speed**: Comparing its convergence time against RIP.

## References
- [GeeksforGeeks – Difference between RIP and OSPF](https://www.geeksforgeeks.org/difference-between-rip-and-ospf/)
- [LINK-PP – In-Depth Comparison](https://www.link-pp.com/knowledge/rip-vs-ospf-link-pp-network-solutions.html)
- [Atlas – Algorithm Comparison](https://www.atlas.org/solution/55c4aa79-4b32-4784-9c63-be79b5706a16/compare-rip-and-ospf-routing-algorithms-on-the-following-aspects-algorithm-type-metric-convergence-time-and-scalability)
