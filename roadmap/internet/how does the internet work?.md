the internet works by connecting devices and computer systems together using a set of standardised protocols. protocols define how information is exchanged between devices and ensure that data is transmitted reliably and securely.

the core of the internet is a global network of interconnected routers, which are responsible for directing traffic between different devices and systems. when data is sent over the internet, it is broken into small packets that are sent from a device to a router. the router examines the packet and forwards it to the next router in the path towards its destination.

to ensure the packets are sent and received correctly, a wide range of other technologies and protocols are used to enable communication and data exchange over the internet such as:
- domain name system (DNS)
- hypertext transfer protocol (HTTP)
- secure sockets layer/transport layer security (SSL/TLS)

# internet addresses
each computer connected to the internet must have a unique address, known as IP address, where IP stands for internet protocol. they are in the form **x.x.x.x** where *x* must be a number from *0-255*.

# protocol stack
the protocol stack used on the internet is referred to as TCP/IP.

| layer | comments |
| :--: | :---: |
| application | protocols specific to applications such as WWW, FTP, HTTP, etc. |
| transmission | TCP directs packets to a specific application on a computer using a port number |
| network | IP directs packets to a specific computer using an IP address |
| physical | converts binary packet data to network signals and back |

# references
- https://cs.fyi/guide/how-does-internet-work
- http://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm
