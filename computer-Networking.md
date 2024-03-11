# Network

## OSI Model (Open Systems Interconnection) [🌐](https://www.geeksforgeeks.org/open-systems-interconnection-model-osi/)[🌐](https://www.baeldung.com/cs/osi-packets-vs-frames#:~:text=A%20frame%20is%20the%20data,they%20encapsulate%20the%20data%20payload.)

- [__Physical Layer__](https://www.geeksforgeeks.org/physical-layer-in-osi-model/)
- [__Data Link Layer__](https://www.geeksforgeeks.org/data-link-layer/)
- [__Network Layer__](https://www.geeksforgeeks.org/network-layer-services-packetizing-routing-and-forwarding/)
- [__Transport Layer__](https://www.geeksforgeeks.org/transport-layer-responsibilities/)
- [__Session Layer__](https://www.geeksforgeeks.org/session-layer-in-osi-model/)
- [__Presentation Layer__](https://www.geeksforgeeks.org/presentation-layer-in-osi-model/)
- [__Application Layer__](https://www.geeksforgeeks.org/application-layer-in-osi-model/)

![OSI model image](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-7-layers.jpg.webp)

![osi image](https://t4tutorials.com/wp-content/uploads/2022/11/which-of-the-following-OSI-layer-is.webp)

### 👉 Physical Layer

- The physical Layer is the bottom-most layer in the OSI Model which is a physical and electrical representation of the system.
- It consists of various network components such as power plugs, connectors, receivers, cable types, etc.
- The physical layer sends data bits from one device(s) (like a computer) to another device(s).
- The physical Layer defines the types of encoding (that is how the 0’s and 1’s are encoded in a signal).

#### Functions Performed by Physical Layer [🔗](https://www.scaler.com/topics/computer-network/physical-layer-in-osi-model/)

1. Topologies
1. Configuration
1. Transmission Modes
1. Hardware Layer
1. Bits synchronization
1. Bits rate control
1. Baseband and Broadband transmissions

#### Physical Topologies or Network Topology

- There are the four types of physical topology-
    1. Mesh Topology
    1. Star Topology
    1. Bus Topology
    1. Ring Topology

#### Line Configuration

- Point-to-Point configuration
- Multi-Point configuration

#### Modes of Transmission Medium

1. Simplex mode
1. Half Duplex mode
1. Full-Duplex mode

### 👉 Data Link Layer

- The data link layer is the second layer from the bottom in the OSI network architecture model
- It is responsible for the node-to-node delivery of data.
- Its major role is to ensure error-free transmission of information.
- DLL is also responsible for encoding, decode and organizing the outgoing and incoming data.

#### Sub-layers of the Data Link Layer

The data link layer is further divided into two sub-layers

- __Logical Link Control (LLC)__
- __Media Access Control (MAC)__

#### Functions of the Data-link Layer

1. Framing
1. Addressing
1. Error Control
1. Flow Control
1. Access Control

#### Protocols in Data link layer

There are various protocols in the data link layer, which are as follows:

1. Synchronous Data Link Protocol (SDLC)
1. High-Level Data Link Protocol (HDLC)
1. Serial Line Interface Protocol (SLIP)for encoding
1. Point to Point Protocol (PPP)
1. Link Access Procedure (LAP)
1. Link Control Protocol (LCP)
1. Network Control Protocol (NCP)

### 🌟Framing

### 🌟Addressing

### 🌟Error Control

### 🌟Flow Control [🔗](https://www.scaler.com/topics/computer-network/flow-control-and-error-control/)

Flow control is a set of procedures that restrict the amount of data a sender should send before it waits for some acknowledgment from the receiver.

- Flow Control is an essential function of the data link layer.
- It determines the amount of data that a sender can send.
- It makes the sender wait until an acknowledgment is received from the receiver’s end.

Methods of Flow Control are __Stop-and-wait__ , and __Sliding window__.

![Methods of Flow Control](https://scaler.com/topics/images/flow-control.webp)

#### Stop-and-wait

Here stop and wait means, whatever the data that sender wants to send, he sends the data to the receiver. After sending the data, he stops and waits until he receives the acknowledgment from the receiver. The stop and wait protocol is a flow control protocol where flow control is one of the services of the data link layer.

Working:

- The sender sends data to the receiver.
- The sender stops and waits for the acknowledgment.
- The receiver receives the data and processes it.
- The receiver sends an acknowledgment for the above data to the sender.
- The sender sends data to the receiver after receiving the acknowledgment of previously sent data.
- The process is unidirectional and continues until the sender sends the End of Transmission (EoT) frame.

![Stop-and-wait protocol works](https://scaler.com/topics/images/stop-and-wait-protocol-in-link-layer.webp)

#### Sliding window

Sliding window protocols are data link layer protocols for reliable and sequential delivery of data frames. The sliding window is also used in Transmission Control Protocol.

Working:

- The sender and receiver have a “window” of frames. A window is a space that consists of multiple bytes. The size of the window on the receiver side is always 1.
- Each frame is sequentially numbered from 0 to n - 1, where n is the window size at the sender side.
- The sender sends as many frames as would fit in a window.
- After receiving the desired number of frames, the receiver sends an acknowledgment. The acknowledgment (ACK) includes the number of the next expected frame.

![Sliding window protocols](https://scaler.com/topics/images/slidong-window-protocol.webp)

#### Error Control

![Error Control](https://scaler.com/topics/images/error-correction-in-link-layer.webp)

1. __Stop-and-wait ARQ(Automatic Repeat Request)__

- In the case of stop-and-wait ARQ after the frame is sent, the sender maintains a timeout counter.
- If acknowledgment of the frame comes in time, the sender transmits the next frame in the queue.
- Else, the sender retransmits the frame and starts the timeout counter.
- In case the receiver receives a negative acknowledgment, the sender retransmits the frame.

![Stop-and-wait ARQ](https://scaler.com/topics/images/stop-and-wait-arq-in-link-layer.webp)

1. Sliding Window ARQ
To deal with the retransmission of lost or damaged frames, a few changes are made to the sliding window mechanism used in flow control.

    1. __Go-Back-N ARQ__ :
    In Go-Back-N ARQ, if the sent frames are suspected or damaged, all the frames are re-transmitted from the lost packet to the last packet transmitted

    ![Go-Back-N ARQ](https://scaler.com/topics/images/go-back-n-arq-in-link-layer.webp)

    1. __Selective Repeat ARQ__:

    Selective repeat ARQ/ Selective Reject ARQ is a type of Sliding Window ARQ in which only the suspected or damaged frames are re-transmitted.

    ![Selective Repeat ARQ](https://scaler.com/topics/images/selective-repeat-arq.webp)

### 🌟Access Control [🔗](https://www.geeksforgeeks.org/multiple-access-protocols-in-computer-network/)

The Data Link Layer is responsible for transmission of data between two nodes. Its main functions are-

- Data Link Control
- Multiple Access Control

__Data Link control__ :- The data link control is responsible for reliable transmission of message over transmission channel by using techniques like framing, error control and flow control.

__Multiple Access Control__ :– If there is a dedicated link between the sender and the receiver then data link control layer is sufficient, however if there is no dedicated link present then multiple stations can access the channel simultaneously. Hence multiple access protocols are required to decrease collision and avoid crosstalk.

#### __Multiple access protocols can be subdivided further as__

![Multiple access protocols](https://media.geeksforgeeks.org/wp-content/uploads/2-44.jpg)

1. __Random Access Protocol__ :- In this, all stations have same superiority that is no station has more priority than another station. Any station can send data depending on medium’s state( idle or busy).

    It has two features:
    1. There is no fixed time for sending data
    1. There is no fixed sequence of stations sending data

    The Random access protocols are further subdivided as:
    1. ALOHA (Areal Locations of Hazardous Atmospheres)
    1. CSMA (Carrier sense multiple access)
    1. CSMA/CD (Carrier sense multiple access with collision detection)
    1. CSMA/CA (Carrier sense multiple access with collision avoidance)

1. __Controlled Access Protocol__ :-In controlled access, the stations seek information from one another to find which station has the right to send. It allows only one node to send at a time, to avoid the collision of messages on a shared medium.

    The three controlled-access methods are:
    1. Reservation
    1. Polling
    1. Token Passing

1. __Channelization Protocol__:-

### 👉 Network Layer

- The network Layer is the third layer in the OSI model of computer networks.
- Its main function is to transfer network packets from the source to the destination.
- It is involved both the source host and the destination host.
- At the source, it accepts a packet from the transport layer, encapsulates it in a datagram, and then delivers the packet to the data link layer so that it can further be sent to the receiver.

#### Features of Network Layer

1. The main responsibility of the Network layer is to carry the data packets from the source to the destination without changing or using them.
1. If the packets are too large for delivery, they are fragmented i.e., broken down into smaller packets.
1. It decides the route to be taken by the packets to travel from the source to the destination among the multiple routes available in a network (also called routing).
1. The source and destination addresses are added to the data packets inside the network layer.

#### Services Offered by Network Layer

The services which are offered by the network layer protocol are as follows:

1. Packetizing

![Packetizing image](https://media.geeksforgeeks.org/wp-content/uploads/20230419121402/Forwarding-2-(2).png)

1. Routing

![Routing image](https://media.geeksforgeeks.org/wp-content/uploads/20230410112203/Forwarding-2.png)

1. Forwarding

![Forwarding image](https://media.geeksforgeeks.org/wp-content/uploads/20230410112108/Forwarding-1.png)

#### Other Services Expected from Network Layer

1. Error Control
1. Flow Control
1. Congestion Control

### 👉Transport Layer

<img align="right" width="300" height="200" src="https://static.javatpoint.com/tutorial/computer-network/images/transport-layer.png">

- The transport Layer is the second layer in the TCP/IP model and the fourth layer in the OSI model.
- It is an end-to-end layer used to deliver messages to a host.
- It is termed an end-to-end layer because it provides a point-to-point connection rather than hop-to-hop, between the source host and destination host to deliver the services reliably.

#### Working of Transport Layer

The transport layer takes services from the Application layer and provides services to the Network layer.

- __At the sender’s side:__ The transport layer receives data (message) from the Application layer and then performs Segmentation, divides the actual message into segments, adds the source and destination’s port numbers into the header of the segment, and transfers the message to the Network layer.

- __At the receiver’s side:__ The transport layer receives data from the Network layer, reassembles the segmented data, reads its header, identifies the port number, and forwards the message to the appropriate port in the Application layer.

#### Responsibilities of a Transport Layer

- The Process to Process Delivery
- End-to-End Connection between Hosts
- Multiplexing and Demultiplexing
- Congestion Control
- Data integrity and Error correction
- Flow control

#### Protocols of Transport Layer

1. Transmission Control Protocol (TCP)
1. User Datagram Protocol (UDP)
1. Stream Control Transmission Protocol (SCTP)
1. Datagram Congestion Control Protocol (DCCP)
1. AppleTalk Transaction Protocol (ATP)
1. Fibre Channel Protocol (FCP)
1. Reliable Data Protocol (RDP)
1. Reliable User Data Protocol (RUDP)
1. Structured Steam Transport (SST)
1. Sequenced Packet Exchange (SPX)

### 👉Session layer [🔗](https://www.educative.io/answers/session-layer-in-osi-model)

- The session layer, known as layer 5 in the OSI model, plays a pivotal role in establishing, managing, and terminating sessions between two devices.
- A session resembles a logical connection that facilitates the organized exchange of data. This layer ensures that data transfer remains orderly, synchronized, and error-free, even during interruptions.

#### Session Layer Protocols

1. AppleTalk Data Stream Protocol ([ADSP](https://www.geeksforgeeks.org/adsp-fullform/))
1. Real-time Transport Control Protocol ([RTCP](https://www.geeksforgeeks.org/real-time-transport-control-protocol-rtcp/))
1. Point-to-Point Tunneling Protocol ([PPTP](https://www.geeksforgeeks.org/pptp-full-form/))
1. Password Authentication Protocol ([PAP](https://www.geeksforgeeks.org/password-authentication-protocol-pap/))
1. Remote Procedure Call Protocol ([RPCP](https://www.geeksforgeeks.org/remote-procedure-call-rpc-in-operating-system/))
1. Sockets Direct Protocol (SDP)

## TCP/IP Model [🌐](https://www.geeksforgeeks.org/tcp-ip-model/?ref=lbp)

- __Application Layer__
- __Transport Layer(TCP/UDP)__
- __Network/Internet Layer(IP)__
- __Data Link Layer (MAC)__
- __Physical Layer__

![diagrammatic comparison of the TCP/IP and OSI model](https://www.imperva.com/learn/wp-content/uploads/sites/13/2020/02/OSI-vs.-TCPIP-models.jpg.webp)

### 🌟 Error Detection in computer Network [🌐](https://www.geeksforgeeks.org/error-detection-in-computer-networks/)

Error is a condition when the receiver’s information does not match the sender’s information. During transmission, digital signals suffer from noise that can introduce errors in the binary bits traveling from sender to receiver. That means a 0 bit may change to 1 or a 1 bit may change to 0.

#### Types of Errors

1. __Single-Bit Error__
1. __Multiple-Bit Error__
1. __Burst Error__
