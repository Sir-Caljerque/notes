Basically a wall, or filet that allows and disallows network traffic in/out of a network
Could be physical computer systems, or software

firewalls look at packet headers and compare them with the existing firewall rules ( sequential )

Different types:
- **Packet filtering**
	- Most common
	- examines header information of data packets
		- IP source/dest
		- Diretion - in/out
		- TCP or UDP
- Static filtering
- Dynamic filtering
- Stateful inspection
	- Not only looks at the tables, but also maintains a table for established outbound connections
	- TCP
		- once the handshake is confirmed, the connection is ongoing until connection is closed
	- For example
		- **Deny** all traffic coming to 127.0.0.1
		- **Deny** all traffic going from 127.0.0.1
		- **Allow** any connection from  10.0.0.* on any port >1023
- NAT firewall
	- used to prevent external traffic sniffers to learn internal IP and port numbers
	- made because number of IPv4 addresses were runnung out
		- PC@10.0.0155:6100 <-> Router@71.221.36.199:5000 <-> serverHost
- Application gateways
	- Usually installed on dedicated computer AKA *proxy server* (or *reverse proxy*)
- Circuit gateways
	- Transport layer
	- Similar to stateful inpection
	- Prevents direct connections between one network and another
		- Creates tunnels connecting specific processes or systems on each side of the firewall
- MAC layer firewalls
	- operate at the MAC layer of the OSI model
	- considers specific host computer's ID in its filtering decisions
	- Operates with ACL enctris that black/whitelist certain host MAC addresses
- Hybrid firewalls
	- combine elements of other types of firewalls, or combine 2+ firewalls

Firewalls are categorized by structure

