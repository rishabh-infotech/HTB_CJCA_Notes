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
