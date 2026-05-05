# Proxies

- A proxy is when a device sits in the middle of a connection and act as a mediator. 
- **The mediater** is the critical peice of information because it means the device in the middle must be able to inspect the content of the traffic.
- Without the ability to be a mediatore, the device is technically a gateway, not a proxy.
- Proxies will almost always operate at Layer 7 of the OSI Model.

**There are many types of proxies, but the key ones are :**
  - Dedicated proxy / Forward Proxy
  - Reverse Proxy
  - Transparent Proxy

## Dedicated Proxy / Forward Proxy :
  - A forward proxy is when a client makes a request to a computer, and that computer carries out the request.
- A forward proxy is a server that sits between client devices and the internet, when a client sends a request to access a website or online resource, the request is directed to proxy first then proxy forwards to the destination server.
      
   - **Example 1 :** In a corporate network, sensitive computers may not have direct access to the internet, To access a website, they must go through a proxy.
      - using proxy is powerful line of defence against malware, because For malware to work, it required connection  with attacker server to receive task and for this it uses C2 =command & control. But Proxy blocked direct connection, so Malware must 1- Bypass proxy or 2- understand proxy setting.
      - Browser like CHrome, Edge and internet explorer uses **Windows System Proxy** automatically, so malware uses Winstock (Windows network API) to bypass it and easily bypass proxy.
      - But **Firefox** is different it uses **libcurl** and in this case malware have to extract setting manually.
        
    - **Example 2 :** Alternatively malware could use DNS as C2=(command & control)
        - But if company monitors DNS using tools Sysmon, suspicious traffic gets detected quickly.
          
    - Another Example is **Burp suite :**
      - It is a proxy tool used for -
        - Intercept HTTP traffic
        - Modify traffic
        - Security testing (pentesting)
      - It can act as Foraward proxy , reverse proxy and transparent proxy .
      - **That's why it's called "swiss Army Knife of HTTP Proxies".**
<P align="center"><img width="2576" height="1000" alt="forward_proxy" src="https://github.com/user-attachments/assets/a8ec6b55-257b-496d-a7d2-fa4d1033b3bb" /></P>


   ## Reverse Proxy :

   - Instead of being designed to filter outgoing requests, it filters incoming ones.
   - The most common goal of a Reverse Proxy, is to listen on an address and forward it to a closed off network.
   - Many organization use Cloudfare. It works as reverse proxy, sits between user and traffic, filters traffic and protects from DDos attacks, Bots and malicious requests.
   - By using cloudfare, organization have a way to filter the amount of traffic that gets sent to their observers.
   - Attacker infect a machine in a company and then create that machine reverse proxy, which bypass firewall, Hide attacker identity and Avoid logging systems.
   - If any organization have IDS(Intrusion Detection System) it can detect incoming traffic, so attacker take acces using ssh, then a reverse proxy can send web request and bypass(evade) IDS.
   - Common Reverse proxy is **ModSecurity**, it is a Web Application Firewall (WAF).
   - **Web Application Firewall** inspect web requests for malicious content and block the request if it is malicious.
   -  Cloudfare can also work as WAF but it needs to decrypt https traffic and some organization don't want this.
<p align='center'><img width="2576" height="1000" alt="reverse_proxy" src="https://github.com/user-attachments/assets/c39319e4-b424-4130-b574-84687070c8b5" /></p>

  ## (Non-) Transparent Proxy :
  All these proxies srvices act either *transparently* or *non-transparently*

  - **Transparent Proxy :**
    - The client does not know about its existence.
    - The transparent proxy intercepts the client's communication request to the internet.
    - Outside both transparent and non-transparent proxy acts as communnication partener.

  - **Non- Transparent proxy :**
    - We(Client) must be informed about its existence.
    - The software we want to use are given a special proxy configuration that ensures all traffic goes through the proxy.
    - Proxy provide the only path to other network, so there is no direct connection available, all traffic goes through proxy.
    - Communication to the internet is generally cut off without a corresponding proxy configuration. 
