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

### Layers

1. **Application :** This layer controls the input and output of data and provides the application functions. 
2. **Presentation :** This layer's task is to transfer the system-dependant presentation of data into a independent form of data. 
3. **Session :** The session layer controls the logical connection between two systems. (Connection, Prevention and termination).
4. **Transport :** This layer is used for end -to-end control of the transferred data. The transport layer can detect and avoid congestion situations and segment data streams.
5. **Network :** On the network layer, Connection is established in **circuit-switched networks** and data packets are forward in **packet switched networks**. Data is transmitted over the entire network from the sender to the reciever. <br/>
   **Circuit-switched network :** A fixed path is created before sending data.
   <img width="2392" height="984" alt="packet_switching" src="https://github.com/user-attachments/assets/0b184d3e-9bfe-413f-8d39-099836be743c" /><br/>
  **Packet-switched Network :** Data is broken into small packets and each packets can take different paths, no fixed connection is required.
   <img width="773" height="335" alt="packet_switching" src="https://github.com/user-attachments/assets/2b4c59a6-9af9-430d-a206-0979cfb7b423" />

6. **Data Link Layer :** The main task of this layer is to enable reliable and error free transmissions on the respective medium by uding MAC.
7. **Physical Layer :** The transmission takes place on wired or wireless transmission. It transmit data physically in raw bitstreams.

### Note
  - **Layer 2-4 are transport oriented, and the layer 5-7 are application oriented layers.** <br/>
  - **If two systems communicate, OSI model runs atleat two times.**


