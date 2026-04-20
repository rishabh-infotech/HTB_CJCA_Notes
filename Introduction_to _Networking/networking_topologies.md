# Networking Topologies

- A netwrok topology is a typical arrangement and phyical or logical connection of devices in a network. 
- Computers are hosts, such as clients and servers.
- They include network component (switches, bridges and router), which have distribution function and ensure that all network hosts can establish logical connection with each other.
- Network topology determines the component to be used and the access methods to the transmission media.
- **Transmission medium layout** (used to connect devices) is the physical topology of the network, this refers to the cabling plan, the position of the nodes and the connection between the nodes and the cabling. **Logical topology** is how the signals act on the network media or how the data will be transmitted across the network from one device to the devices' physical connection.

**We can devide the entire network topology area into three areas:**

## 1. Connections :

- **Wired Connecttion :** Coaxial cabling,  Glass fiber cabling, Twisted-pair cabling.
- **Wireless Connection :** Wi-Fi, Cellular, Satellite.

## 2. Nodes - Network Interface Controller (NICs) :

- Network nodes are the **transmission medium's connection points** to transmitters and receivers of electrical, optical, or radio signals in the medium.
- Example : Repeaters,   Hubs,  Bridges,  Switches,  Router/Modem,  Gateways,  Firewalls.

## 3. Classifications :

- We can imagine a topology as a **virtual form** or **structure of a netwrok**.
- These topologies can be either **physical** or **logical**.
- For example, the computers on a LAN may be arranged in a circle , but it is not necessary they have ring topology.

**Network topologies are devided into the following eight basic types :**
  1. P2P
  2. Bus
  3. Star
  4. Ring
  5. Mesh
  6. Tree
  7. Hybrid
  8. Daisy Chain

### P2P :
- The simplest netwrok topology with a dedicated connection between two hosts is the point-to-point topology.
- In this, a direct and straightforward physical link exists only between two hosts.
<img width="1477" height="438" alt="topo_p2p" src="https://github.com/user-attachments/assets/0ff95d95-aa9e-405e-bbd9-6dbef70dad4e" />

### BUS :
- All hosts are connected via a same transmission medium and every host has access to transmission medium and the signals that are transmitted over it.
- The transmission medium for this can be, **coaxial cable**.
- Since the medium is shared with all the others, only **one host can send**, and all the others can only receive and evaluate the data and see whether it is intended for itself. 
<img width="2576" height="1294" alt="topo_bus" src="https://github.com/user-attachments/assets/7854b198-8a8d-4a23-9161-10b0b3eef944" />

### Star :
- Star topology is a network component that maintains a connection to all hosts.
- Each host is connected to the **central network component** via a separate link, this usually a router a hub or a switch.
- These (router, hub, switches) handle the **forwarding function**(the process of passing a request, packet or data from a sender to designated server without processing it).  
- The data traffic on the central network component can be very high since all data and connection go through it. 
<img width="2576" height="1000" alt="topo_star" src="https://github.com/user-attachments/assets/bfa44cfb-5a10-4201-bd93-402835dc5778" />

### Ring :
- The physical ring topology is such that each host or node is connected to the ring with two cables.
  - One for the incoming signals.
  - Another for the outgoing ones.
- Ring topology does not require an active network component, the control and access to the transmission medium are regulated by a protocol to which all stations adhere.
- A logical ring topology is based on a physical star topology.
- The transmission medium is accessed sequentially from station to station using a retrieval system from the central station or a **token**.
- A token is a bit pattern that continuously passes through a ring network in one direction, which works according to the claim token process.  
<img width="2576" height="1000" alt="topo_ring" src="https://github.com/user-attachments/assets/4e37d28f-4ab3-42a8-8f19-4e7e6e522bd0" />

### Mesh :
- Many nodes decide about the connection on a physical level and the routing on a logical level in meshed networks, therefore meshed structure have no fixed topology.
- There are two basic concept: fully meshed and the partially meshed.
- Each host is connected to every other host on **Fully meshed** network, this technique is primarily used in WAN or MAN for high bandwidth.
- In the **partially meshed structure**, the endpoint are connected by only one conncetion, specific nodes are connected to exactly one other node, and some other nodes are connected to two or more other nodes with a P2P connection. 
<img width="2576" height="1000" alt="topo_mesh" src="https://github.com/user-attachments/assets/40f6db26-3440-4020-98c0-d350dca42539" />

### Tree :
- Tree topology is an extended star topology that have more extensive local network in this structure.
- This is specially usefull when several topologies are combined.
- This topology is often used in larger company buildings, and also used for broadband networs and city netwroks(MAN).
<img width="2576" height="1000" alt="topo_tree" src="https://github.com/user-attachments/assets/4c352463-b370-4df6-8378-e868e19b17bb" />

### Hybrid :
- Hybrid networks combined two or more topologies so that the resulting network does not present any standard topologies.
- For example, a tree network can represent a hybrid topology in which star networks are connected via interconnected bus network.
<img width="2576" height="1000" alt="topo_hybrid" src="https://github.com/user-attachments/assets/6f3bea1c-1a2c-4bd7-aee9-efd855b62e14" />

### Daisy Chain :
- In this, multiple hosts are connected by placing a cable from one node to another.
- This create a chain of connection, so its also known as daisy chain configuration, in which multiple hardware components are connected in a series. This type of networking is found in automation technology.
- Daisychaining is based on the physical arrangement of the nodes which are structural and can be made independent of the physical layout.
- The signal is sent to and from a component via its pevious nodes to the computer system.
<img width="2576" height="1000" alt="topo_daisy-chain" src="https://github.com/user-attachments/assets/72b5ef4a-6fb8-47b9-bbd4-0e8b957c1df7" />




