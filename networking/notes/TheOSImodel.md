#  The 7-layers of the OSI Model

## Open Systems Interconnection Model

The OSI model is a theoretical model of networking. It's a framework that shows us how a packet/data traverses through a network in seven different layers. 

This communication model provides a framework that simplifies the way devices and apps communciate over a network, ensuring that all devices/apps can understand one another.

## Why do we need a communication model?

1. **Application independence**

- This means that the functions of each layer in the OSI Model operate independently of one another.
- Therefore, changes or issues in one layer do not directly affect the others.
- This modular approach allows for flexibility and adaptability in networking.

This means:

- applications (e.g. web browsers, email, or games) can work on top of the network without worrying about how data is physically sent or routed 

This is important because the application only needs to worry about its own job e.g displaying a web page, while others handle tasks like data transport or error checking.

2. **Simplified Network Equipment Management**

- upgrading netwrok equipment can be very difficult if there isn't a standard model, it is much easier if everything speaks the same language

3. Decoupled innovation

- innovations can happen in each layer indepndently, without affecting the entire system
- layer-specific netwrok improvement leads to faster and more efficient advancements 

## The 7 layers

| **Layer**  | **Description** | **Function** | **Example** |
|------------|-----------------|--------------|-------------|
| **Layer 1 - Physical** | The actual hardware that sends data as electrical signals. | Transmits raw bit stream over a physical medium | Cables, switches, fiber, hubs, repeaters |
| **Layer 2 - Data Link** | Ensures error-free data transfer between two devices on the same network using MAC addresses. | Provides node-to-node transfer and error detection/correction. | Computer to router, switches, bridges |
| **Layer 3 - Network (IP)** | Decides the best path to send data across different networks using IP addresses. | Manages packet forwarding and routing through intermediate routers. | IP addresses, routers |
| **Layer 4 - Transport (TCP/UDP)** | Ensures reliable data transfer between devices using protocols like TCP or UDP. | Provides reliable data transfer and reassembles data. | TCP, UDP, ports |
| **Layer 5 - Session** | Manages the connection and communication between two devices. | Establishes, maintains, and terminates sessions. | Session management protocols (LinkerD) |
| **Layer 6 - Presentation** | Translates data into a format applications can understand (e.g., encryption, compression). | Ensures data is in a usable format for the application layer. | Encryption, compression |
| **Layer 7 - Application** | Where the user interacts (e.g., web browsers, email applications). | Provides network services directly to end-user applications. | HTTP, HTTPS, FTP, SMTP |



### TCP/IP model
- the backbone of the internet
- condensed format of the OSI (4Ls)
  - This model is another version that focuses on layers 3/4 & 7.
  - Explains how data is packaged, sent and recieved over a network, from users application down to the physical network connection.

| **The 4 Layers**               | **Description**                                                                                 | **Example**                                             |
|-------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| **Application Layer**    | This is where network applications and protocols operate - HTTP, TLS, DNS                     | Web browsing, sending emails                            |
| **Transport Layer**      | Ensures data is sent reliably (using TCP) or quickly (using UDP), depending on the requirement. | TCP for reliability, UDP for speed                      |
| **Internet Layer**       | Responsible for logical addressing and routing data between networks using IP addresses - IP                                           | IP addressing, routing                                  |
| **Network Access Layer** | Manages the physical connection to the network, whether it's via cables, Wi-Fi, or other means. | Ethernet, Wi-Fi, Wireless, LAN                                      |
