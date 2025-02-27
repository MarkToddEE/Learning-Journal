# OTJ 
## User Datagram Protocol (UDP)

UDp is a communication protocol used over IP
It is connectionless as it doesn't need to set up a connection to the destination before it send the data. It doesn't cater for error correction (ie lost packets).
There are no retransmissions of dropped data packets or guarntee of delivery. As such it is a quicker transmission method than TCP.

It does however use checksums to validate the integrity of each data packet header and data. If the checksum fails, the packet is dropped (with no resend requested)

In a UDP datagram, there is provision to define the source port and the destination port. The source port is optional (set to 0 if undefined). The source port is used if any reply is expected. The destination port is needed to direct the data to the correct port on the destination machine
