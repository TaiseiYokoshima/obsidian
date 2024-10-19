
It utilizes INT which is appended to ip packets right after ip header.

INT contains congestion status (queue size) of each link that the packet traversed.

In the case of TCP, the INT is added to the ack packet.

PHCC congestion algo, controls the packets in-flight (window) rather than the sending rate.

It adjusts window based on the bottleneck link

- is PHCC implemeneted at NIC hardware? or by the os?
- Should I know the components of the NIC?
- 



