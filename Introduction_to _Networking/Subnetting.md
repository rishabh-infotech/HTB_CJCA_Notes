# Subnetting 

- Division of an IPv4 network into subnetwork, is called subnetting.
- Subnet is a logical division of a network.
- Division of a network happen only in $2{^n}$, where n=1,2,3,....
  - example : $2{^2}$ = 4 subnet, $2{^5}$ = 32 subnet and so on.
- Key idea of subnetting is to fix bits from host address, to make internal network address.
- The value of n calculate above is the number of bits to be fixed.
  - example :<br/>
  IP Address : 192.168.0.0 - 11000000 &nbsp; 10101000 &nbsp; 00000000 &nbsp; 00000000</br>
  Default Subnet : 255.255.255.0 - 11111111 &nbsp; 11111111 &nbsp; 11111111 &nbsp; 00000000
  - First 24 bit is default network address and 8 bit is host address.
  - Now , we want to make **2 Subent** then 2<sup>1</sup>
  - It means we add 1 bit more from host address as network address, putting value '0' in first time and '1' in second time.</br>
    IP Address :  1100000 &nbsp; 10101000 &nbsp; 0000000 &nbsp; ${\color{red}0}0000000$ - red bit is going to fixed ${\color{red}"0"}$ in first subnet and ${\color{red}"1"}$ in second subnet.
  - Total usable host = 2<sup>8</sup> = 256 host .
  - 256 host distribute in two subnetwork - each gets 128 host.
  - These 2 IP ranges will be :<br/>
    ```yaml
    - 1st Subnet : 11000000  10101000  00000000  00000000    to    11000000  10101000  00000000  01111111
                      192       168        0         0                192       168        0        127
    
    - 2nd Subnet : 11000000  10101000  00000000  10000000    to    11000000  10101000  00000000  11111111
                      192       168        0        128               192       168        0        255
    ```
  - Subnet mask of internal subnetwork is : We set host bit '1' in default subnet.
    ```text
    Subnet Mask : 11111111  11111111  11111111  100000000
                    255       255       255        128
- All IPs :
  ```yaml
  Default Network : 192.168.0.0
  Default Broadcast : 192.168.0.255

  1st Subnetwork address: 192.168.0.1
  Broadcast Address : 192.168.0.127

  2nd Subnetwork : 192.168.0.128
  2nd Broadcast Address : 192.168.0.255
  ```
  $\color{orange}{\text{Note : Default network address and first subnetwork address is same, similarly second subnetwork broadcast address and}}$
  $\color{orange}{\text{default broadcast address is also same.}}$ <br/>
   $\color{orange}{\text{But, Default Address is for outer network, and subnetwork address is for internal network.}}$ </br>
  $\color{orange}{\text{First the packet came at outer router(Default) and then it send to internal router who decide packets}}$
  $\color{orange}{\text{destination according to internal address.}}$
