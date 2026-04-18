# RIP (Routing Information Protocol)

RIP is a distance-vector routing protocol used in many small to medium-sized networks.

## Key Features (RIP v2)
- **Algorithm**: Distance-vector (Bellman-Ford).
- **Metric**: Hop count (the number of routers to reach a destination).
- **Limits**: Maximum of 15 hops; a hop count of 16 is considered unreachable.
- **Updates**: Sends periodic updates (every 30 seconds) to its neighbors.
- **Convergence**: Relatively slow compared to link-state protocols.

## Usage in Lab 3
In this lab, you will enable RIP v2 on all routers to measure:
- How long the network takes to stabilize after a link failure (Convergence Time).
- The amount of packet loss during the failure and recovery period.

## References
- [TutorialsPoint – RIP vs OSPF](https://www.tutorialspoint.com/article/difference-between-rip-and-ospf)
- [ComputerNetworkingNotes – RIP V/s OSPF Differences](https://www.computernetworkingnotes.com/ccna-study-guide/rip-v-s-ospf-differences-between-rip-and-ospf.html)
