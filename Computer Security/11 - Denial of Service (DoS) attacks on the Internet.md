# Denial-of-Service (DoS)
- A form of attack on the availability of some service
- Categories of resources that could be attacked are:
	- network bandwidth
		capacity of network links. for most organizations, their link to their ISP
- System resources
- Application resources
	- e.g. predefined limits on valid requests 


# First Generation DoS Attacks
#### Flooding Ping Command
- By using ping's flooding option, it sends packets as fast as they can
- overwhelm the capacity of the network
- source of the attack is clearly identified unless a spoofed address is used
- affects network performance drastically

#### TCP Handshake attack
- Once a syn packet is received, a tcp control block is created in the os memory.
- sending a flood of syn packets with increasing source port identifiers will quickly overrun the table










