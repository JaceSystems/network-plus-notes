# OSI Model

## Layer 1 - Physical layer (bits)

- This layer describes the physical signals being sent out. Ethernet cables, etc.

## Layer 2 - Data Link Layer (frames)

- Used to connect two devices on a network. Uses MAC address to communicate. Uses Switches, etc.

## Layer 3 - Network Layer (packets)

- Determines how to forward traffic by looking at the IP address. Fragment frames to traverse across network and put them together on the other side.
- IP addresses, Routers, Packets

## Layer 4 - Transport Layer (Segments)

- Ability to transport information from one device to another
- protocals: TCP and UDP. Taking large amounts of data and putting into smaller pieces then putting them back together on the other side.
- TCP Segment UDP datagram

## Layer 5 - Session Layer (Data)

- Communication management between devices
- Typically anything related to starting, stopping, and restarting can be associated with this layer
- Control Protocols, tunneling protocols

## Layer 6 - Presentation Layer (Data)

- Character encoding, Application encryption. Just prior to us seeing it on screen
- Application encrypting (SSL/TLS)

## Layer 7 - Application Layer (Data)

- What we see with our eyes
- HTTP, HTTPS, FTP, DNS, POP3, etc.

# Networking Devices

## Router (Layer 3)

- Data from one IP subnet to another IP subnet. Could be on same area or across the world
- Diverse network types can be connected - LAN, WAN, copper, fiber

## Switch (Layer 2)

- Hardware operated. ASIC. Forwards traffic based on data link address or MAC address. Meant for communication across locally. May provide PoE.

## Firewalls (Layer 3)

- Traditional firewalls filter traffic by TCP or UDP port number. Modern ones use NGFW which is able to identify applications traversing network and able to manage if allowed or not allowed on network. Can encrypt traffic going across network and very common to have firewalls at one remote site and another remote site and create encrypted tunnel between the firewalls.
- Can act as a router. NAT (network address translation) and dynamic routing protocols

## IDS AND IPS

- Watches network traffic. Looking for attacks inbound to network
- Exploits against OS and applications. Take advantage of known vulns to systems
- IDS is able to alarm and alert if sees attacks
- IPS is able to actually block traffic it finds suspicious

## Load Balancer

- Distribute the loads across multiple servers
- Helps maintain uptime and availability
- Users access a service and server. The load balancer actually distributes the load to multiple servers to perform as fast as possible.
- Data can be cached on load balancer so information can come even faster rather than going all the way to servers.

## Proxies

- Manage connections between users and servers by using proxy.
- Recieves the users request and send the request on their behalf. Useful for caching information, URL filtering, access control, content scanning. Prevents malicious software.

## NAS VS SAN

- Network attached storage - connect to a shared storage device acros the netwok (file-level access)
- Storage Area Network - Looks and feels like a local storage device
- CONS requires lots of bandwidth

## Access Point

- Allows us to connect wirelessly to network.
- Ethernet connection attached to the access point and this provides wireless connection opportunities. Large business buildings need multiple. Settings and policies may need to be managed.
- Seamless roaming should be possible so they are always connected to network

## Wireless LAN controller

- Single pane of glass for managing network
- Helps with deploying new access points
- Performance and security monitoring
- Configure and deploy change to all sites
- Report an access point use
- Paired with access points from same manufacturer


# Encapsulation At Each Layer

- Layer 1 - No encapsulation. Deals with physical transmission of bits
- Layer 2 - Encapsulates data into frames with MAC addresses
- Layer 3 - Adds headers with source and destination IP addresses
- Layer 4 - Adds headers with source and destination port numbers, sequence, and acknowledgement numbers
- Layer 5 - Adds session identifiers to maintain state
- Layer 6 - Adds headers for data format and encryption details
- Layer 7 - Data is prepared for transmission, but no headers are added yet


