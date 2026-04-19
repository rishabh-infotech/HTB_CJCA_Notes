# Netwrok Types

## Common Terminology :

- **Wide Area Network (WAN) :** Internet.
- **Local Area Network (LAN) :** Internal Network.
- **Wireless Area Network (WLAN) :** Internal netwrok accessible over WI-Fi.
- **Virtual Private Network (VPN) :** Connects Multiple network sites to one.

### WAN :
- WAN is just a large number of LANs joined together.
- When dealing with networking equipment, we will often have a WAN address and LAN address.
- Many large companies or government agencies will have an "Internal WAN" (Also called Intranet, Airgap Netwoork).
- The primary way to identify if the netwok is WAN or not is:
  - WAN specific routing protocol such as Border Gateway Protocol (BGP).
  - IP Schema in use is not within RFC 1918.
    - **IP Schema :** Structured plan of assigning IP addresses in network.
    - **RFC 1918 :** RFC 1918 is a rule developed by **Internet Engineering Task Force(IETF)** that defines private IP adress range inside a local network, means rserved IP adresses to use only witihn a local network. RFC 1918 defines three private IP Ranges: **10.0.0.0/8**, **172.16.0.0/12**, **192.168.0.0/16** .

### LAN/WLAN :
- LAN and WLAN will typically assign IP Addresses designated for local use in three ranges: **10.0.0.0/8**, **172.16.0.0/12**, **192.168.0.0/16**.
- In some cases we can assign routable IP addresses such as (College, Hostel), but less common in use.
  - **Routable IP Addresses :** IPs which are public IPs, travels accross Internet through routers.

### VPN :
There are three main types of VPN, but all three have the same goal of making the user feel as if they were plugged into different network.

- **Site-to-Site VPN :**
  - Both client and server are Netwrok Devices, Typically either **Routers** or **Firewalls**.
  - This is most commonly used to join company networks together over the network, allowing multiple location to communicate each other.
  
- **Remote Access VPN :**
  - It creates virtual interface that behaves as it is on a client's network.
  - Routing Table(List of available possible path from source to destination, we choose shortest one) is created when joining the VPN.
  - If the VPN only creates routes for specific network, this is called a **Split-Tunnel VPN**, meaning internet connection is not going out of the VPN.
  - Split-tunnel is not ideal for organizations as network based detection not worked when the traffic goes out the internet.

- **SSL VPN :**
  - These are becoming increasingly common as web browser are becoming capable of doing anything.
  - Typcally these will stream application or entire desktop sessions to your web browser securily.
 
### Global Area Netwrok (GAN) :
- A worldwide network such as the Internet.
- Internationally active companies also maintain isolated network that span saveral WANs and connect company computers worldwide.

### Metropolitan Area Network (MAN) :
- MAN is a broadband telecommunication network that connects several LAN in a geographical area.
- Internationally operating netwrok operators provide the infrastructure for MAN.
- HIgh performances routers and connections based on optical fibre are used, provide significantly higher data throughput.

### PAN/WPAN :
 - Modern end devices can be connected ad hoc(decentralized wireless netwrok) to form a netwrok to enable data exchange.
 - A wireless coneection formed using bluetooth called **piconet**.
 - It's range exyend only a few meter.
 - In the context of IoT WPAN are used to communicate control and monitor application with low data rates. Protocols such as Insteon, Z-Wavw and ZigBee were explicitly designed for smart home and automation. 
 
 
