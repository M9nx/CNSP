
source from => https://www.geeksforgeeks.org/tcp-ip-model/

TCP/IP   stands for  ==Transmission Control Protocol/Internet Protocol==

TCP/IP was designed and developed by the Department of Defense (DoD)

The main work of TCP/IP is to transfer the data of a computer from one device to another

![[Pasted image 20250125015410.png]]


### How TCP/ IP works?

- TCP/IP employs the client-server demonstration of communication in which a client or machine (a client) is given a benefit (like sending a webpage) by another computer (a server) within the network.
- Collectively, the TCP/IP suite of conventions is classified as stateless, which suggests each client request is considered new since it is irrelevant to past requests. Being stateless liberates up network paths so they can be utilized continuously.
- The transport layer itself, is stateful. It transmits a single message, and its connection remains open until all the packets in a message have been received and reassembled at the destination.
- The TCP/IP model differs from the seven-layer Open System Interconnection (OSI) model designed after it.

## Layers of TCP/IP Model

- Application Layer
- [Transport Layer(TCP/UDP)](https://www.geeksforgeeks.org/tcp-and-udp-in-transport-layer)
- Network/Internet Layer(IP)
- Network Access Layer


## 1. Network Access Layer

a group of applications requiring network communications.
responsible for generating the data and requesting connections.

## 2. Internet or Network Layer

responsible for the logical transmission of data over the entire network

main protocols => IP |  ICMP | ARP

==IP== => responsible for delivering packets from the source host to the destination host by looking at the IP addresses in the packet headers.

has 2 versions: IPv4 and IPv6.
IPv6 is growing as the number of IPv4.

==ICMP== => stands for Internet Control Message Protocol

responsible for providing hosts with information about network problems.

==ARP== => stands for Address Resolution Protocol
Its job is to find the hardware address of a host from a known IP address.


==The Internet Layer== is responsible for routing packets of data from one device to another across a network.


example ==> Imagine that you are using a computer to send an email to a friend. When you click “send,” the email is broken down into smaller packets of data, which are then sent to the Internet Layer for routing. The Internet Layer assigns an IP address to each packet and uses routing tables to determine the best route for the packet to take to reach its destination. The packet is then forwarded to the next hop on its route until it reaches its destination. When all of the packets have been delivered, your friend’s computer can reassemble them into the original email message.

In this example, the Internet Layer plays a crucial role in delivering the email from your computer to your friend’s computer. It uses IP addresses and routing tables to determine the best route for the packets to take, and it ensures that the packets are delivered to the correct destination. Without the Internet Layer, it would not be possible to send data across the Internet.


## 3. Transport Layer

exchange data receipt acknowledgments and retransmit missing packets to ensure that packets arrive in order and without error.

End-to-end communication is referred to as such.

TCP => Transmission Control Protocol
UDP => User Datagram Protocol

Applications that transport little amounts of data use UDP rather than TCP because it eliminates the processes of establishing and validating connections.


## 4. Application Layer

responsible for end-to-end communication and error-free delivery of data.

==HTTP== => Hypertext transfer protocol
 it is a combination of HTTP with SSL(Secure Socket Layer). 

==SSH== => stands for Secure Shell
maintain the encrypted connection. It sets up a secure session over a TCP/IP connection.

==NTP== => stands for Network Time Protocol
used to synchronize the clocks on our computer to one standard time source.


The ==host-to-host layer==  => responsible for providing communication between hosts (computers or other devices) on a network.
It is also known as the transport layer.

Some common use cases for the host-to-host layer include:

- ==Reliable Data Transfer:== The host-to-host layer ensures that data is transferred reliably between hosts by using techniques like error correction and flow control. For example, if a packet of data is lost during transmission, the host-to-host layer can request that the packet be retransmitted to ensure that all data is received correctly.

- ==Segmentation and Reassembly==: The host-to-host layer is responsible for breaking up large blocks of data into smaller segments that can be transmitted over the network, and then reassembling the data at the destination. This allows data to be transmitted more efficiently and helps to avoid overloading the network.

- ==Multiplexing and Demultiplexing==: The host-to-host layer is responsible for multiplexing data from multiple sources onto a single network connection, and then demultiplexing the data at the destination. This allows multiple devices to share the same network connection and helps to improve the utilization of the network.

- ==End-to-End Communication==: The host-to-host layer provides a connection-oriented service that allows hosts to communicate with each other end-to-end, without the need for intermediate devices to be involved in the communication.

==Example==: Consider a network with two hosts, A and B. Host A wants to send a file to host B. The host-to-host layer in host A will break the file into smaller segments, add error correction and flow control information, and then transmit the segments over the network to host B. The host-to-host layer in host B will receive the segments, check for errors, and reassemble the file. Once the file has been transferred successfully, the host-to-host layer in host B will acknowledge receipt of the file to host A.

In this example, the host-to-host layer is responsible for providing a reliable connection between host A and host B, breaking the file into smaller segments, and reassembling the segments at the destination. It is also responsible for multiplexing and demultiplexing the data and providing end-to-end communication between the two hosts.


The physical layer is ==not== covered by the TCP/IP model because the data link layer is considered the point at which the interface occurs between the TCP/IP stock and the underlying network hardware.


## Other Common Internet Protocols

TCP/IP Model covers many Internet Protocols. The main rule of these Internet Protocols is how the data is validated and sent over the Internet. Some Common Internet Protocols include:

- ==FTP (File Transfer Protocol)==:  takes care of how the file is to be sent over the Internet.
- ==SMTP (Simple Mail Transfer Protocol)==:  is used to send and receive data.


![[Pasted image 20250125034747.png]]



### Which IP Addresses Do TCP/IP Work With?

> TCP/IP generally works with both the IP that is, and .
>  If you are using IPv4 or IPv6, it seems that you are already working on TCP/IP Model.

### How many layers are in the TCP/IP Model?

> The TCP/IP Model has four layers:
> 
> - Network Interface Layer
> - Internet Layer
> - Transport Layer
> - Application Layer

### What does each layer do?

> - ****Network Interface Layer****: Handles the physical transmission of data over a network.
> - ****Internet Layer****: Manages the routing of data packets across the network.
> - ****Transport Layer****: Ensures reliable data transmission between devices.
> - ****Application Layer****: Provides protocols for specific data communication services on a process-to-process level.

### How is the TCP/IP Model different from the OSI Model?

> The OSI Model has seven layers, while the TCP/IP Model has four layers. The TCP/IP Model is simpler and more practical, making it more widely used in real-world networking.

### What are the main protocols in the TCP/IP Model?

> Key protocols include:
> 
> - ****TCP (Transmission Control Protocol)****: Ensures reliable data transmission.
> - ****IP (Internet Protocol)****: Handles addressing and routing of data packets.
> - ****HTTP/HTTPS****: Used for web communication.
> - ****FTP****: Used for file transfers.
> - ****SMTP****: Used for email communication.

### What is the role of IP addresses in the TCP/IP Model?

> IP addresses identify devices on a network, enabling data to be routed to the correct destination.


----
---

