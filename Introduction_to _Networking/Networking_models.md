# Networking Models

Two Networking models describe the communication and transfer of data from one host to another, called 
1. OSI/ISO Model 
2. TCP/IP Model.


## Packet Transfers

### PDU
- PDU stands for Protocol data unit.
- PDU is a data unit, exchanged  between layers in a netwrok (OSI Model).
- A layer create it's PDU by adding own header in previous layer's PDU.
- Present working layer, treat previous layer PDU as data.

**Example :**
1. Application Layer's PDU = Data
2. Transport Layer's PDU = Segment = Data + Transport Header, Where Data is PDU of Session Layer.
<img width="2576" height="1000" alt="net_models_pdu2_updated" src="https://github.com/user-attachments/assets/19f7d6ff-9597-4312-9b37-a945a68e9cf0" />

- During transmission , each layer adds header to the PDU from the upper layer, this process is called encapsulation.
- This process continuous to the Physical layer or network layer, where data is transmitted to the reciever.
- The reciever reverses the process and unpacks the data on each layer with the header information.
<img width="2650" height="959" alt="packet_transfer" src="https://github.com/user-attachments/assets/72bec02f-6b30-4182-ac6e-0cb834945798" />

# OSI Model
- The goal of OSI standard was to create a reference model that enables the communication of different technical systems.
- The OSI model uses 7 different layer, based on each other to achieve this goal.
- The standard was created to trace how a connection is structured and established visually.
- OSI Model is a theoretical model used for understanding networking.

### Layers

1. **Application :** serves as direct interface between software user and network.
   - provide an interface to display information access from other layers or host.
   - Enables users to log into and interact with remote hosts caleed **Network Virtual Terminal**
   - Provides the framework for users to retrieve, manage and manipulate files.
   - Offers distributed database access to manage global information.
3. **Presentation :** ensures that data is formatted, secure and compressed
   - It extract data from application layer and converts it into a standardized format for network transmission.
   - Handles the media encoding using JPEG, MPEG, GIF.
   - Provide security by using SSL/TLS - converting plain text into cipher text (Encryption).
   - Reduces total number of bits required for data transmission , increases network efficiency and speed, this process caledd **compression**. 
4. **Session :** The session layer controls the logical connection between two systems.
   - Manages the establishment, maintenance and termination of connection between applications.
   - Ensure the connecting parties are secure and verified.
   - Inserts checkpoints into the data stream, This allows to resume the failed data transfer from it's previous checkpoint.
5. **Transport :** ensure end to end delivery of entire messages.
   - data is broken down into smaller chunks called **segments** .
   - Uses port numbers to ensure data is delivered to the specific process or application, this called **Service point addressing**.
   - TCP ensures message is received in sequence, even when packet is reached using packet switching - this is achieved by **reassembling** of packets in reciever end.
   - **TCP** requires handshake to establish connection and provide connection oriented, reliable and ordered connection.
   - In other hand **UDP** sends data immediately without formal connection, It provide connection-less, fast, unordered connection.
6. **Network :** On the network layer, Connection is established in **circuit-switched networks** and data packets are forward in **packet switched networks**. Data is transmitted over the entire network from the sender to the reciever. <br/><br/>
   **Circuit-switched network :** A fixed path is created before sending data.
   
   <img width="2392" height="984" alt="packet_switching" src="https://github.com/user-attachments/assets/0b184d3e-9bfe-413f-8d39-099836be743c" /><br/><br/>
  **Packet-switched Network :** Data is broken into small packets and each packets can take different paths, no fixed connection is required.
   
   <p align="center"> <img width="773" height="335" alt="packet_switching" src="https://github.com/user-attachments/assets/2b4c59a6-9af9-430d-a206-0979cfb7b423" /><p/>

   - Data segments are encapsulated into packets.
   - Assign unique IP address(logical addressing) to indentify devices globally and packet reached their correct destination.
   - Determine the most efficient and shortest path, this process called **Routing**.
   - Primarily implements via **Routers and Switches**.  

7. **Data Link Layer :**
   - The main task of this layer is to enable reliable and error free transmissions on the respective medium by uding MAC.
   - Data packets received from network layer divided into manageable units by adding specific "start" and "stop" bits, called Framing.
   - This Layer uses physical addressing (MAC) to identify host. And Encapsulates the sender's and receiver's MAC addresses into the frame header.
   - It manages Error Control, Flow Control and Access Control.
   - Ther are two sublayer 1. Logical Link Control - Manages flow and error control. 2. Media Access Control - Determines how devices physically access the transmission medium and handles hardware addressing.
8. **Physical Layer :**
    - This layer transmits and receives actual raw bitstream.
   - It ensures **Bit Synchroization -** sender and receiver are in sync by providing a clock signal, that controls the timing of bit transmission.
    - **bit rate control -** dictates the transmission speed, defined as the number of bits sent per second.
    - **Transmission Mode -** determines direction of flow of data - Simplex, duplex and half duplex.  

### Note
  - **Layer 2-4 are transport oriented, and the layer 5-7 are application oriented layers.** <br/>
  - **If two systems communicate, OSI model runs atleat two times.**

# TCP/IP Model

- TCP/IP model is also a layered reference model, often reffered as Internet Protocol Suite.
- TCP/IP stands for two protocols TCP and IP. **IP** is located within the **Netwrok Layer** and **TCP** is located within he **Transport Layer** .
- TCP/IP is a practical protocol-driven model used for actual internet communication.

### Layers :

**4. Application :** 
  - The application layer allows application to access the other layers services and defines the         protocols use to exchange data.
  - It merges Three Layer (Application, Presentation and Session) and works all of three.
  - It provide an interface to communicate with lower layer.
  - Handle data formatting, so both sender and reciever correctly understood.
  - Provide encryption for secure communication.
  - Manages session to track ongoing connection.

**3. Transport :**
  - The Transport Layer is responsible for providing TCP Session and and UDP datagram services for       the Application Layer.
  - Segmentation, Reliabe Delivery & Error Handling, Fast Communication, Flow Control,         Multiplexing.

**2. Internet :**
  - The Internet Layer is responsible for addressing, packaging and routing data packets so they can travel across networks and reach the correct destination device.
  - Provide Logical Addressing, Packet Routing, Fragmentation and Reassembly, Protocol Support.

**1. Link :**
  - The link layer is responsible for placing the TCP/IP packets on the network medium and receiving corresponding packets from the netwrok medium.
  - Responsible for physically transmitting data over network hardware, including cables, switches or wireless.
  - It handles Physical Transmission, Framing, Error Addresssing, MAC Addressing, Access Control.
<img width="2576" height="1000" alt="image" src="https://github.com/user-attachments/assets/d30a54df-10df-42e4-8f1e-d25e6f61bb52" />

### Most Important Task of TCP/IP 

1. Logical Addressing (IP) : Logical addressing in the network layer uses unique virtual addresses, such as IP addresses, to identify devices across different networks, enabling communication.
2. Routing (IP)(Network Layer) : when a packet transmit in network each middle router of path determine next router which enable shortest path for that packet. This process is called routing.
3. Error and control flow (TCP) : The sender and receiver are frequently in touch, checking connection is still established or packet transmission error by sending control messages.
4. Name Resolution : DNS provide name resolution through Fully Qualified Domain (FQDN) in IP addresses.

## Working of TCP/IP Model 

### Sender to receiver :
- **Application :** The user's software create data and passes it to next layer.
- **Transport :** The data is broken into segments, and TCP or UDP adds control information to ensure reliable delivery.
- **Internet Layer :** Each segment is encapsulated into packets with IP addresses.
- **Link Layer:** The packets are converted into frames suitable for the physical network and transmitted over the cables or wireless signals.

### At destination :
- **Link Layer :** The frames are received from the physical medium and checked for errors.
- **Internet :** Frames are unpacked to extract packets and use IP adress to ensure it reaches correct device.
- **Transport :** Segments are reassembled into the original message, and any missing or corrupted data is corrected(if TCP is used).
- **Application :** Complete data is deliverd to the user application. 
<p align='center'><img width="800" height="400" alt="working-of-tcp" src="https://github.com/user-attachments/assets/83aa9ebf-0029-43ab-afd6-bb6480fd37b5" /></p>
