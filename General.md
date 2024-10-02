# Client
- tun device captures all outgoing traffic
- vpn sessions decides if it is
	- server initiated -> do not route and send to network via raw socket
	- client initiated -> route with udp tunnel that is excluded from tun routing


# Server
-  upon device connection, distribute a private ip and add it to the tun
- 
