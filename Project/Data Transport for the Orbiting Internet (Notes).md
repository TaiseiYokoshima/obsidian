OrbtTCP utilizes in-network telemetry (INT) to obtain per-hop congestion information for each of its active subflows running on edge-disjoint paths. 

OrbtTCP enables network operation with low buffer capacity and low latency for end hosts, maximizes application throughput and network utilization, and swiftly reacts to network hotspots due to bursty traffic or path reconfiguration. 

With OrbTCP, data is transported through multiple edge-disjoint (not necessarily equal-cost) paths that are always available in LEO satellite networks. 

We draw inspiration from existing data center approaches that attempt to minimize flow latency for short flows. We employ in-network telemetry (INT) to obtain per-hop satellite queue information, allowing the sender to adjust the congestion window according to the current network load, separately for each one of its subflows. We have implemented a simulation model of OrbTCP and compare its performance to traditional loss and delay-based data transport protocols.

In OrbTCP, data is sent through multiple subflows that operate on edge-disjoint paths of similar base RTTs; i..e., quasi-equal-cost paths. 

LEO satellite networks consist of many such paths for every pair of end hosts. In its current iteration, OrbTCP adopts an uncoupled congestion control approach where subflows operate independently to each other. This prevents unfairness between multiple subflows sharing a link with other single-path connections. 

Each packet carries an INT header which is populated by both the sender and satellites on the path to its destination. The sender appends the last calculated RTT. Each satellite appends a timestamp indicating the time at which the packet departed the outgoing interface as well as the current outgoing buffer occupancy in bytes, total number of transmitted bytes and out-going link bandwidth. Each satellite also maintains a smoothed moving average of RTT values and the number of flows (N) it has observed within a given time window and appends such values in the packets' INT header. Note that satellites do not maintain per-flow state. INT information is echoed back to the sender by having the receiver copying it to respective acknowledgements. 