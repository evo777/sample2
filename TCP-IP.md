# TCP/IP
- The two core (and most well known) protocols  of the Internet Protocol Suite, sometimes used synonymously with the IPS
- TCP is a transport-layer protocol, that abstracts away the packet handling intricacies of the internet layer from the application
- IP is an internet-layer protocol that is responsible for encapsulating data as packets and sending them over network(s) from one host to another
- Search "Internet Protocol Suite" or "OSI model" for an explanation of these abstraction layers and how they fit together
  - IPS has four layers: link layer (e.g. ethernet), internet layer (e.g. IPv4), transport layer (e.g. TCP, UDP), and application layer (e.g. HTTP)

### Transmission Control Protocol (TCP)
- Purpose is to reliably and accurately stream data  as octets between the application and the IP layer
- **Reliable**
  - Provides the sender notification of receipt and requests for lost or discarded packets
  - Sender will also automatically re-send packets based on acknowledgement timeouts 
- **Ordered**
  - Through a sequence number, TCP will rearrange packets out of order data
- **Error checked**
  - Through use of a checksum
- WWW, email, and FTP are examples of applications (running in the application layer) that rely on TCP
- Optimized for accurate delivery
  - may incur long delays while waiting for missing / requested packets
  - not a good protocol for latency-sensitive applications such as VoIP and video streaming (see UDP instead)


### Internet Protocol (IP)
- Purpose is to deliver datagrams (packets) from the source host to the destination host across one or more IP networks, based on the IP addresses in the packet headers
- Defines the packet structures that encapsulate the data
- Takes care of packet fragmentation and reassembly
- Utilizes a best effort delivery model - reliability is not guaranteed and is the responsibility of upper layer protocols like TCP
- IPv4 and the newer IPv6 (128-bit addressing, among other new features) are the two versions in use today

### A note about WebSockets
- You may have used Socket.io, which is an API wrapper for WebSockets (and several other technologies)
- HTTP based applications communicate over a series of multiple TCP connections, while WebSockets are based on a single, longer-lived TCP connection
- WebSockets reduces the overhead of opening and closing connections
  - Benefits some applications which would otherwise overburden the server with requests (e.g. a real-time chat app constantly polling the server for updates is bad)
  - The server can, instead, simply push the data to the client over the already-open connection.