transmission control protocol is used on top of IP to ensure reliable transmission of packets.

# process of transmission
## step 1: establish connection
when 2 computers want to send data to each other over TCP, they first need to establish a connection using a 3-way handshake.

![establishing connection](https://cdn.kastatic.org/ka-perseus-images/d09f9d37ff2a2deb21a8822f8c99ba6b86319f0b.svg)

- first computer sends a packet with SYN (synchronise) bit set to 1
- second computer sends back a packet with the ACK (acknowledge) plus the SYN bit set to 1
- first computer replies back with an ACK

![TCP header](https://cdn.kastatic.org/ka-perseus-images/9a4a79816965be53e1071cf6b0e2991cb4d170ca.svg)

3 packets involved in the 3-way handshake do not typically include any data.

## step 2: send packets of data
when a packet of data is sent over TCP, the recipient must always acknowledge what they received.
- first computer sends a packet with data and a **sequence number**
- second computer acknowledges it by setting the ACK bit and increasing the **acknowledgement number** by the length of the received data

those 2 numbers help the computers to keep track of which data was successfully received, and which data was lost.

## step 3: close the connection
either computer can close the connection when they no longer want to send or receive data.
- a computer initiates closing the connection by sending a packet with the FIN (finish) bit set to 1
- other computer replies with an ACK and another FIN
- after 1 one ACK from the initiating computer, the connection is closed

# detecting lost packets
TCP connections can detect lost packets using a timeout
- after sending off a packet, the sender starts a timer and puts the packet in a re-transmission queue
- if the timer runs out and the sender has not yet received an ACK from the recipient, it sends the packet again

# handling out of order packets
TCP connections can detect out of order packets using the sequence and acknowledgement numbers.

when the recipient sees a higher number than what they have acknowledged so far, they know that they are missing at least one packet in between. the recipient lets the sender know that something is missing by sending a packet with an acknowledgement number set to the expected sequence number.

the recipient can use the sequence numbers to re-assemble the packet data in correct order.

# references
- https://www.khanacademy.org/computing/computers-and-internet/xcae6f4a7ff015e7d:the-internet/xcae6f4a7ff015e7d:transporting-packets/a/transmission-control-protocol--tcp
