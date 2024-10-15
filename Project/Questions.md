- Is the main approach of congestion control in HPCC is to pause the data flow of upstream so that packet loss it prevented for sensitive data such as RDMA, so that the sender's timer is triggered which drops the sending rate
- HPCC directly controls the number of inflight bytes - how is this done? doesn't it just pause upstream flow
- "each packet a sender sends will be acknowledged by the receiver" - does this mean ack is sent for ip packets? or is this talking abt tcp?
- 



