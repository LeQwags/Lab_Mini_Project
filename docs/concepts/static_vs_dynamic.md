# Static vs. Dynamic Routing

Understanding the trade-offs between static and dynamic routing is a core requirement for Lab 3.

## Static Routing
- **Manual Configuration**: Routes are manually entered into the routing table by the administrator.
- **Characteristics**:
  - Simple and predictable.
  - Very low overhead (uses minimal CPU and bandwidth).
  - Routes do not change unless manually updated.
- **Disadvantage**: Does not automatically reroute if a link fails; requires manual intervention for recovery.
- **Best Use**: Small, stable networks with few routers.

## Dynamic Routing
- **Protocol-Driven**: Routers run a routing protocol (like RIP or OSPF) to exchange information and build their routing tables automatically.
- **Characteristics**:
  - Automatically updates when the network topology changes.
  - Adapts to link failures and network growth.
  - Uses more CPU and bandwidth for protocol overhead.
- **Best Use**: Larger or complex networks where manual configuration is impractical.

## Comparative Resources
- [GeeksforGeeks – Static and Dynamic Routing](https://www.geeksforgeeks.org/computer-networks/difference-between-static-and-dynamic-routing/)
- [IO River – Static vs Dynamic Routing: What’s The Difference](https://www.ioriver.io/blog/static-dynamic-routing)
- [Indeed – Comparison Guide](https://www.indeed.com/career-advice/career-development/dynamic-routing-vs-static-routing)
- [Ruijie – Definitions, Pros and Cons](https://www.ruijie.com/en-global/support/faq/dynamic-route-vs-static-route)
