

OSI => Open Systems Interconnection

explains how different computer systems communicate over a network.

OSI Model was developed by the International Organization for Standardization (ISO)****.

## Layers of the OSI Model

There are 7 layers in the OSI Model and each layer has its specific role in handling data. All the layers are mentioned below:

- Physical Layer
- Data Link Layer
- Network Layer
- Transport Layer
- Session Layer
- Presentation Layer
- Application Layer

## Layer 1 – Physical Layer


The lowest layer of the OSI reference model is the ****Physical Layer****.
responsible for the actual physical connection between the devices.

contains information in the form of ****bits.****

responsible for transmitting individual bits from one node to the next.

signal received and convert it into 0s and 1s.

Common physical layer devices are [Hub](https://www.geeksforgeeks.org/what-is-network-hub-and-how-it-works/), [Repeater](https://www.geeksforgeeks.org/repeaters-in-computer-network/), [Modem](https://www.geeksforgeeks.org/difference-between-modem-and-router/), and [Cables](https://www.geeksforgeeks.org/types-of-ethernet-cable/).

### Functions of the Physical Layer

- ****Bit Synchronization:**** The physical layer provides the synchronization of the bits by providing a clock. 


- ****Bit Rate Control:**** The Physical layer also defines the transmission rate i.e. the number of bits sent per second.


- ****Physical Topologies:**** Physical layer specifies how the different, devices/nodes are arranged in a network i.e. [bus topology](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-bus-topology/), [star topology](https://www.geeksforgeeks.org/advantages-and-disadvantages-of-star-topology/), or [mesh topology](https://www.geeksforgeeks.org/advantage-and-disadvantage-of-mesh-topology/).


- ****Transmission Mode:**** Physical layer also defines how the data flows between the two connected devices. The various transmission modes possible are [Simplex, half-duplex and](https://www.geeksforgeeks.org/difference-between-simplex-half-duplex-and-full-duplex-transmission-modes/) full duplex.

## Layer 2 – Data Link Layer (DLL)

 responsible for the node-to-node delivery of the message.
 make sure data transfer is error-free from one node to another, over the physical layer.
 responsibility of the DLL to transmit it to the Host using its [MAC address](https://www.geeksforgeeks.org/mac-address-in-computer-network).
 Packet in the Data Link layer is referred to as Frame.
 [Switches and Bridges](https://www.geeksforgeeks.org/difference-between-switch-and-bridge/) are common Data Link Layer devices.


The Data Link Layer is divided into two sublayers:

- [Logical Link Control (LLC)](https://www.geeksforgeeks.org/logical-link-control-llc-protocol-data-unit)
- [Media Access Control (MAC)](https://www.geeksforgeeks.org/introduction-of-mac-address-in-computer-network)


****NIC (****[****Network Interface Card)****](https://www.geeksforgeeks.org/nic-full-form/).

The Receiver’s MAC address is obtained by placing an ARP ([Address Resolution](https://www.geeksforgeeks.org/how-address-resolution-protocol-arp-works) Protocol) request onto the wire asking, “Who has that IP address?” and the destination host will reply with its MAC address.

### Functions of the Data Link Layer

- ****Framing:**** Framing is a function of the data link layer. It provides a way for a sender to transmit a set of bits that are meaningful to the receiver. This can be accomplished by attaching special bit patterns to the beginning and end of the frame.

- ****Physical Addressing:**** After creating frames, the Data link layer adds physical addresses (MAC ****addresses)**** of the sender and/or receiver in the header of each frame.


- ****Error Control:**** The data link layer provides the mechanism of error control in which it detects and retransmits damaged or lost frames.


- ****Flow Control:**** The data rate must be constant on both sides else the data may get corrupted thus, flow control coordinates the amount of data that can be sent before receiving an acknowledgment.


- ****Access Control:**** When a single communication channel is shared by multiple devices, the MAC sub-layer of the data link layer helps to determine which device has control over the channel at a given time.

## Layer 3 – Network Layer

The network layer works for the transmission of data from one host to the other located in different networks. 
The sender and receiver’s IP [address](https://www.geeksforgeeks.org/what-is-an-ip-address) are placed in the header by the network layer.
Segment in the Network layer is referred to as Packet
Network layer is implemented by networking devices such as [routers and switches](https://www.geeksforgeeks.org/difference-between-router-and-switch/).

### Functions of the Network Layer

- Routing: The network layer protocols determine which route is suitable from source to destination. This function of the network layer is known as routing.


- Logical Addressing: To identify each device inter-network uniquely, the network layer defines an addressing scheme. The sender and receiver’s IP addresses are placed in the header by the network layer. Such an address distinguishes each device uniquely and universally.


## Layer 4 – Transport Layer

takes services from the network layer.
The data in the transport layer is referred to as Segments.
responsible for the end-to-end delivery of the complete message.

Protocols used in Transport Layer are [TCP](https://www.geeksforgeeks.org/what-is-transmission-control-protocol-tcp/), [UDP](https://www.geeksforgeeks.org/user-datagram-protocol-udp/) [NetBIOS](https://www.geeksforgeeks.org/what-is-netbios-enumeration/), [PPTP](https://www.geeksforgeeks.org/pptp-full-form/).


****At the sender’s side****, the transport layer receives the formatted data from the upper layers, performs ****Segmentation****, and also implements ****Flow and error control**** to ensure proper data transmission. It also adds Source and Destination [port number](https://www.geeksforgeeks.org/what-is-ports-in-networking) in its header and forwards the segmented data to the Network Layer.


****At the Receiver’s side,**** Transport Layer reads the port number from its header and forwards the Data which it has received to the respective application. It also performs sequencing and reassembling of the segmented data.


### Functions of the Transport Layer

- ****Segmentation and Reassembly:**** This layer accepts the message from the (session) layer and breaks the message into smaller units. Each of the segments produced has a header associated with it. The transport layer at the destination station reassembles the message.
- ****Service Point Addressing:**** To deliver the message to the correct process, the transport layer header includes a type of address called service point address or port address. Thus, by specifying this address, the transport layer makes sure that the message is delivered to the correct process.

### Services Provided by Transport Layer

- [Connection-Oriented Service](https://www.geeksforgeeks.org/connection-oriented-service)
- [Connectionless Service](https://www.geeksforgeeks.org/connection-less-service)


## Layer 5 – Session Layer

responsible for the establishment of connections, management of connections, terminations of sessions between two devices.

provides authentication and security.

Protocols used in the Session Layer are NetBIOS, PPTP.



### Functions of the Session Layer

- ****Session Establishment, Maintenance, and Termination:**** The layer allows the two processes to establish, use, and terminate a connection.
- ****Synchronization:**** This layer allows a process to add checkpoints that are considered synchronization points in the data. These synchronization points help to identify the error so that the data is re-synchronized properly, and ends of the messages are not cut prematurely, and data loss is avoided.
- ****Dialog Controller:**** The session layer allows two systems to start communication with each other in half-duplex or full duplex.


![Pasted image 20250125201700](https://github.com/user-attachments/assets/0d78a732-b5b9-42ea-ace2-7fe6c30b32bc)



## Layer 6 – Presentation Layer

called the Translation layer.
he data from the application layer is extracted here and manipulated as per the required format to transmit over the network.

Protocols used in the Presentation Layer are JPEG, MPEG, GIF, TLS/SSL, etc.

### Functions of the Presentation Layer

- ****Translation:**** For example, [ASCII to EBCDIC](https://www.geeksforgeeks.org/difference-between-ascii-and-ebcdic).

- ****Encryption/ Decryption:**** Data encryption translates the data into another form or code. The encrypted data is known as the ciphertext, and the decrypted data is known as plain text. A key value is used for encrypting as well as decrypting data.

- ****Compression:**** Reduces the number of bits that need to be transmitted on the network.

## Layer 7 – Application Layer

implemented by the network applications.
Protocols used in the Application layer are SMTP, FTP, DNS, etc.

![Pasted image 20250125220049](https://github.com/user-attachments/assets/8d864439-0031-404f-a757-464f4c947990)



### Functions of the Application Layer

The main functions of the application layer are given below.

- ****Network Virtual Terminal (NVT):**** It allows a user to log on to a remote host.

- ****File Transfer Access and Management (FTAM):**** This application allows a user to access files in a remote host, retrieve files in a remote host, and manage or control files from a remote computer.

- ****Mail Services:**** Provide email service.

- ****Directory Services:**** This application provides distributed database sources and access for global information about various objects and services.



## How Data Flows in the OSI Model?

When we transfer information from one device to another, it travels through 7 layers of OSI model. First data travels down through 7 layers from the sender’s end and then climbs back 7 layers on the receiver’s end.

Data flows through the OSI model in a step-by-step process:

- ****Application Layer:**** Applications create the data.
- ****Presentation Layer:**** Data is formatted and encrypted.
- ****Session Layer:**** Connections are established and managed.
- ****Transport Layer:**** Data is broken into segments for reliable delivery.
- ****Network Layer:**** Segments are packaged into packets and routed.
- ****Data Link Layer:**** Packets are framed and sent to the next device.
- ****Physical Layer:**** Frames are converted into bits and transmitted physically.


![Pasted image 20250125220913](https://github.com/user-attachments/assets/254a716a-ea08-4668-95b2-9b681060a01a)



![Pasted image 20250125221215](https://github.com/user-attachments/assets/27f48f1f-de7c-4c1b-b1a1-9ff8b661144b)



## Frequently Asked Questions on OSI Model – FAQs

### ****Can OSI layers work independently?****

> No, OSI layers do not work independently. Each layer depends on the services provided by the layer below it and, in turn, provides services to the layer above it. This layered approach ensures that data is transmitted smoothly from the source to the destination.

### ****How does the OSI Model help in troubleshooting network issues?****

> By breaking down communication into layers, the OSI Model helps network administrators isolate problems more easily.

### ****What happens if a layer in the OSI Model fails?****

> If a particular OSI layer fails, data transmission may be disrupted or fail entirely. Network administrator will check layer by layer to identify and resolve the issue, make sure that each layer is functioning correctly or not.

### ****How does DNS fit into the OSI Model?****

> The Domain Name System (DNS) operates at Layer 7 (Application Layer). It translates domain names into IP addresses, facilitating communication between users and services across the network.


----
---
