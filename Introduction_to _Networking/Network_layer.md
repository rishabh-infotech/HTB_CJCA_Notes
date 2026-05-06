# Network Layer

- The network layer (Layer 3) of OSI controls the exchange of data packets.
- Data packets cannot be directly routed to the receiver and therefore have to be provided with routing nodes.
- The data packets transferred from node to node (this process is called **Hopping**), until they reach their target.
- To implement this process, Every Router identifies destination address of packets, according to this creates a path and decide where to send, which route is shortest and congestion free .
- This process is done in every router of path, from where packets are transmitting.
- It controls data flows rate to avoid congestion.
- In this layer, there is no any data processing happen, It only care about destination address of packet.
- By using dstination address, routers decide path and create routing table(all possible path info).

  ## Protocols

  - Prtocols are defined in each layer of OSI.
  - These protocols represent a collection of rules for communication in respective layer.
  - Protocols of the layers are transparent above or below.
  - Some protocols works on multiple layer(Two or more than two).
  - Most used protocols on this layer
    - IPV4/IPV6
    - IPsec (Internet Protocol Security)
    - ICMP (Internet Control Message Protocol)
    - IGMP (Internet Group Message Protocol)
    - RIP (Routing information protocol)
    - OSPF (Open shortest path first)
  
