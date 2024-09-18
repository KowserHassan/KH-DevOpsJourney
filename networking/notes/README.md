# Networking Notes

**Networking** refers to the practice of connecting **computers** and other devices (such as phones, printers, and servers) to enable communication and resource sharing.

---

### Why Are Networks Important?
1. **Foundation of Communication**: Networks are the foundation that enables communication between devices.
2. **Resource Sharing**: They allow us to share resources and exchange data (e.g., files, printers).
3. **Internet Access**: Networks enable browsing, streaming, and online communication.
4. **Application Connectivity**: They serve as the backbone for app connectivity and data transfer.

---

### Factors That Influence Networks
- **Geographical Area**: The physical size the network covers (small or large).
- **Number of Users**: The number of devices or people connected.
- **Services**: Types of services available (e.g., file sharing, internet access, applications).

---

### Network Types by Size and Function

**Local Area Network (LAN):**
- **Size**: Small (e.g. home, office, school).
- **Purpose**: Connects devices in a small geographical area for resource sharing.
- **Example**: An office network where multiple computers are connected for file sharing.

**Wide Area Network (WAN):**
- **Size**: Large (spanning cities, countries, or continents).
- **Purpose**: Connects multiple LANs and MANs over a large geographical area.
- **Example**: The internet is the largest WAN.

<img width="655" alt="Screenshot 2024-09-17 at 08 10 28" src="https://github.com/user-attachments/assets/53c5f940-6136-4017-96f1-2ba5231f1d3d">

---

### Networking in DevOps

1. Server interaction - communcation between servers and apps
2. Deployment of apps and updating them
3. Management and monitoring infrastructure 
4. Optimisation - enhances troubleshooting performance and scalability 

---

### Backbone of networks:

| Device    | Function                                                        | Example                                    |
|-----------|------------------------------------------------------------------|--------------------------------------------|
| Switch    | Connects multiple devices within a LAN and ensures efficient dataflow between them | Connects phones, printers, and laptops etc    |
| Router    | Directs messages between networks and connects different networks, ensuring data reaches the correct destination | Connects home network to internet |
| Firewall  | Monitors and controls incoming and outgoing network traffic, securing network by enforcing rules and blocking unauthorised access | Protects a company network from external threats |

## IP & MAC addresses

### IP addresses

- **IP address** (internet protocol address) is a unique identifier for devices in a network, allowing devices to locate and communicate with each other over a local network or internet.

  - There are 2 types: 
<img width="685" alt="Screenshot 2024-09-17 at 08 28 17" src="https://github.com/user-attachments/assets/c47594e2-955a-475f-b904-aa228f0968de">

- **IPv4 address:**
  - 32-bit address made up of four sets of numbers separated by dots (e.g. 192.168.1.1)
  - Each group ranges from 0 to 255
  - Used to identify devices on a network, allowing them to communicate with each other.
  - Most common type of IP used on the internet.
  - However, it's gradually being replaced by IPv6 due to the limited number of available IPv4 addresses.

- **IPv6 address:**
  - 128-bit hexadecimal address.
  - Provides a much larger pool of addresses for current and future devices.
  - Simplifies addressing and enhances security features.
  - Transition from IPv4 to IPv6 is essential for the growth of the internet.

#### Why are IPs important?

They provide: 
1. **Unique identification** – IPs uniquely identify devices.
2. **Data routing** – They direct data to and from the correct location e.g when loading a website.
3. **Communication** – IP addresses allow devices to communicate with each other.
4. **Global activity** – They enable billions of devices to connect and share information worldwide.

---

### MAC addresses (Media Access Control Address)

A permanent 48-bit address used for local device identification. Unique identifier assigned to EVERY network interface - fingerprint for network devices 

- Identifies devices on a local network (not over the internet).
- Ensures your device connects to the correct nearby router.
- Different from an IP address, which operates over the internet.
- Operate at data link level of OSI model 

---

## Ports & Protocols: TCP, UDP

### Ports

**Ports** are like doorways on a computer that manage different types of data entering and leaving through the same IP address.

Examples:
- **Port 80**: Web traffic (HTTP)
- **Port 443**: Secure web traffic (HTTPS)
- **Port 25**: Email (SMTP)

Ports organise and facilitate communication between devices which allows applications like web browsers, email programs, and others to work simultaneously.

### Protocols

Protocols are rules/standards that define how data should be sent and recieved over a network.

- This ensures different devices and software communicate properly by following the same set of rules
- Just as people need a common language to understand each other, devices and programs need to follow the same protocol to exchange data correctly

Examples: 
- HTTP: used for transferring web pages.
- FTP: used for transferring files
- SMTP: used for sending emails.

Without ports and protocols, our network communication would not run smoothly!
 
> **Important:** Ports ensure that data reaches the right application on your device while protocols ensure that the data is understandable and properly formatted!

---

## The 2 main protocols

### Transmission Control Protocol (TCP)

TCP is a set of rules that ensures that data from one device reaches another accurately and in the correct order. The postman of the internet!

A connection-oriented protocol establishes a connection between sender and receiver with a handshake to ensure:
- reliability
- error-checking  

This guarantees that packets are delivered in the correct order and without errors.

<img width="655" alt="Screenshot 2024-09-18 at 15 42 10" src="https://github.com/user-attachments/assets/3926eda5-e061-4fdc-bd9a-1da5d0d2ede4">

While TCP is perfect for applications requiring precise data transfer, like web browsing, email, and file transfers, it can be slower than connectionless protocols due to the extra processing and data management.

The **3-step handshake** is used to establish a reliable connection between a client and a server.

1. **SYN (Synchronise)**:
   - **Client** (e.g web browser) sends a SYN packet to the **server** (e.g YouTube) to initiate the connection. This packet includes an initial sequence number (ISN) and signals that the client wants to establish a connection.

2. **SYN-ACK (Synchronise-Acknowledge)**:
   - **Server** responds with a SYN-ACK packet. This packet acknowledges the client's SYN request and includes its own sequence number (ISN) along with an acknowledgment of the client's sequence number.

3. **ACK (Acknowledge)**:
   - **Client** sends an ACK packet back to the **server** to acknowledge the server’s SYN-ACK packet. This completes the handshake and establishes the connection.

After these steps, data transmission can begin between the client and server.

---

### User Datagram Protocol (UDP)

A **connectionless** communication protocol used for time-sensitive applications like gaming, video streaming, or DNS lookups.

- results in speedier communication because it doesn’t establish a connection with the destination before sending data.
- Instead, UDP sends data packets directly without waiting for acknowledgments or ensuring delivery
- therefore it's faster but less reliable than connection-oriented methods.

<img width="655" alt="Screenshot 2024-09-18 at 15 43 50" src="https://github.com/user-attachments/assets/aa326afe-abb1-4004-a7d0-619bc37eea68">

---

### TCP VS UDP

<img width="655" alt="Screenshot 2024-09-18 at 15 45 39" src="https://github.com/user-attachments/assets/a9e8bffd-326d-4d54-9693-c2f7879074c6">

<img width="655" alt="Screenshot 2024-09-18 at 16 01 09" src="https://github.com/user-attachments/assets/268d8796-b330-4747-9349-e616af2aa3c4">

---

### How does your computer determine whether to use UDP or TCP? 

This is based on the needs of the application or service you're using.

1. **Application Requirements**:

   - **TCP**: Used by applications that need reliable, ordered, and error-checked delivery of data. e.g web browsers, email clients, and file transfers
   - **UDP**: Chosen by applications that prioritise speed and can tolerate some data loss. e.g. streaming services, online gaming, and VoIP (Voice over IP).

3. **Port Numbers**:
   - Applications are associated with specific port numbers that define whether they use TCP or UDP. e.g.
    - HTTP typically uses TCP port 80
    - DNS often uses UDP port 53.

4. **Configuration**:
   - Some applications can be configured to use either TCP or UDP based on user settings or performance needs.
   - e.g. a video streaming app might use UDP for live streaming but switch to TCP for video on demand to ensure smooth playback.

5. **Network Protocol Stack**:
   - The OS's network protocol stack handles the choice of TCP or UDP based on the application's request.
   - It follows the protocol specifications and routing rules to manage data transmission accordingly.

---
