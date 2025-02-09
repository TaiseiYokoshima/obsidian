throughput = bytes received (receiving rate, includes protocol headers and re transmission)
goodput = application data sent / over time, bytes received excluding protocol headers and retransmission

1. test the binary on mininet make it work there
2. figure out the sys call time to write or read from udt socket
3. rewrite so it tests one direction at a time
4. measure receiving rate instead of sending rate
5. make tshark work


better test:
instead of querying every 1024 bytes, write or read as much as possible and use 

measuring upstream:
- use tshark on the server side capture incoming packets from the client
- client sends ? GBs of data to server writing as much as possible every time

