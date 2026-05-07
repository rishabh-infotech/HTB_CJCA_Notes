# IP Addresses :

- Each host in the network located can be identified by the MAC addresses, this allows data exchange within this one network.
- If remote host in another network, MAC address is not enough to establish a connection.
- Addressin on the network is done via IPv4 or IPv6 address.
- IPV4 and IPV4 addresses have two sub addresses.
  - 1-Network Addresses
  - 2-Host Addresses
- Router assigns Host part of the IP at home or by an administrator.
- The respective network administrator assigns the network part.
- **On internet this job is done by IANA(Internet Assigned Nummber Authority).**  
- IP address ensure the delivery of data to teh correct reveiver.
- IP Address can address multiple receiver at a time (broadcast a message).
- It must be assure that each IP address assigned only once in a network.

## IPv4 Structure :

    Binary : 0111 1111.0000 0000.0000 0000.0000 0001
    Decimal : 127.0.0.1

  - IPv4 consists 32-bit binary number combined into 4 bytes(consisting of 8-bit groups-octet), octet ranging from 0-255.
  - These representation can represent into dotted decimal to read easily.

### IPv4 address divided into **classes A - E**.

| Class | Netwrok addresses | First Address | Last Addresses | Subnetmask | CIDR | Subnets | IPs |
|-------|-------------------|---------------|----------------|------------|------|---------|-----|
|A|1.0.0.0|1.0.0.1|127.255.255.255|255.0.0.0|/8|127|16777214+2|
|B|128.0.0.0|128.0.0.1|191.255.255.255|255.255.0.0|/16|16384|65534+2|
|C|192.0.0.0|192.0.0.1|223.255.255.255|255.255.255.0|/24|2097152|254+2|
|D|224.0.0.0|224.0.0.1|239.255.255.255|Multicast|Multicast|Multicast|Multicast|
|E|240.0.0.0|240.0.0.1|255.255.255.255|Reserved|Reserved|Multicast|Multicast|

## Subnet Mask :
  - A subnet mask is a 32-bit number used in a network.
  - By using subnet mask we can get host and network part of an IP.
  - Further logical speration of a network is done with the help of **Subnetting**.
    
| Class | Netwrok addresses | First Address | Last Addresses | ${\color{#7EE787}Subnetmask}$ | CIDR | Subnets | IPs |
|-------|-------------------|---------------|----------------|------------|------|---------|-----|
|A|1.0.0.0|1.0.0.1|127.255.255.255|$${\color{#9CCBF2}255.0.0.0}$$|/8|127|16777214+2|
|B|128.0.0.0|128.0.0.1|191.255.255.255|${\color{#9CCBF2}255.255.0.0}$|/16|16384|65534+2|
|C|192.0.0.0|192.0.0.1|223.255.255.255|${\color{#9CCBF2}255.255.255.0}$|/24|2097152|254+2|
|D|224.0.0.0|224.0.0.1|239.255.255.255|$${\color{#9CCBF2}Multicast}$$|Multicast|Multicast|Multicast|
|E|240.0.0.0|240.0.0.1|255.255.255.255|${\color{#9CCBF2}Reserved}$|Reserved|Multicast|Multicast|

## Network and Gateway Addresses :

- In every network or subnetwork first and last IP adress is reserved.
- First one is for network address and last one is for broadcast address.
- The netwrok address identifies entire network or subnet. It is used to calculate subnet and use by router to make routing table and find packets destination network. 
- Gateway address is used communicate with internet. Gateway address is router IP assigned from available IPs pool of network.
- packets are received and transmit to and from this gateway address.

| Class | ${\color{#7EE787}Network \space addresses}$ | ${\color{#7EE787}Gateway \space Address (anyone \space from \space this \space range)}$ | Subnetmask | CIDR | Subnets | IPs |
|-------|-------------------|-------------------------------|------------|------|---------|-----|
|A|${\color{#9CCBF2}1.0.0.0}$|${\color{#9CCBF2}1.0.0.1 - 127.255.255.254}$|255.0.0.0|/8|127|16777214+2|
|B|${\color{#9CCBF2}128.0.0.0}$|${\color{#9CCBF2}128.0.0.1 - 191.255.255.254}$|255.255.0.0|/16|16384|65534+2|
|C|${\color{#9CCBF2}192.0.0.0}$|${\color{#9CCBF2}192.0.0.1 - 223.255.255.254}$|255.255.255.0|/24|2097152|254+2|
|D|${\color{#9CCBF2}224.0.0.0}$|${\color{#9CCBF2}224.0.0.1 - 239.255.255.254}$|Multicast|Multicast|Multicast|Multicast|
|E|${\color{#9CCBF2}240.0.0.0}$|${\color{#9CCBF2}240.0.0.1 - 255.255.255.254}$|Reserved|Reserved|Multicast|Multicast|

# Broadcast Address :

- The broadcast IP address's task is to connect all devices in a network with each other.
- Broadcast in a network is a message that is transmitted to all participants of a network and does not rewuire any acknowledge(response).
- last IP address of a network is broadcast IP address, and by using this host can broadcast message to all participant in network.

| Class | Netwrok addresses | First Address | ${\color{#7EE787}Last \space (Broadcast \space Address)}$ | Subnetmask | CIDR | Subnets | IPs |
|-------|-------------------|---------------|----------------|------------|------|---------|-----|
|A|1.0.0.0|1.0.0.1|${\color{#9CCBF2}127.255.255.255}$|255.0.0.0|/8|127|16777214+2|
|B|128.0.0.0|128.0.0.1|${\color{#9CCBF2}191.255.255.255}$|255.255.0.0|/16|16384|65534+2|
|C|192.0.0.0|192.0.0.1|${\color{#9CCBF2}223.255.255.255}$|255.255.255.0|/24|2097152|254+2|
|D|224.0.0.0|224.0.0.1|${\color{#9CCBF2}239.255.255.255}$|Multicast|Multicast|Multicast|Multicast|
|E|240.0.0.0|240.0.0.1|${\color{#9CCBF2}255.255.255.255}$|Reserved|Reserved|Multicast|Multicast|

## CIDR :

- CIDR stands for Classless Inter Domain Routing.
- Before this network and host part of IP address is fixed in three classes.
- CIDR allows to create Network address of an IP using almost any number of bits.
- we represent CIDR in **"IP/CIDR value"**.
- For Example : 192.168.1.10/17
  - In this first 17 bits of ip address is network address.

- Binary representation of IP
  
  ```text
    192        168         1        10
  11000000   10101000  00000001  00001010

- Subnet mask of /17 :
  ```text
   11111111  11111111  10000000  0000000
      255      255        127       0

- Get Netwrok Address : Performing **AND operation** in between IP and CIDR
  ```text
   11000000  10101000  00000001  00001010
   11111111  11111111  10000000  00000000
   --------------------------------------
   11000000  10101000  00000000  00000000
     192        168       0          0

- Get Broadcast Address :
  - Easiest way of getting broadcast address is calculate total number of host then fill in network address.
  //```text
  - Toatal Network bit : 17 (get from cidr)
  - Remaining Host bit : 2<sup>32-17</sup> = $2^{15}$
  - Network address : 192.168.0.0
  - $2^{8}$ = 256 host can fit in fourth octet (0 - 255) - 192.168.0.0 to 192.168.0.255
  - Remaining $2^{7}$ = 128 host fits in third octate (0 - 127) - 192.168.0.255 to 192.168.127.255
  - last address(Broadcast Address) is : 191.168.127.255

- All Addresses Finding :
 ```yaml
   IP Address : 192.168.1.10
   Subnet Mask : 255.255.127.0
   Netwrok Address : 192.168.0.0
   First Address : 192.168.0.1
   Last Address : 192.168.127.255
   Broadcast Address : 192.168.127.255
