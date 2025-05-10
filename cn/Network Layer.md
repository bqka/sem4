![[Pasted image 20250307084200.png]]
![[Pasted image 20250307084224.png]]
![[Pasted image 20250307084404.png]]
![[Pasted image 20250307084455.png]]
![[Pasted image 20250307085003.png]]
![[Pasted image 20250307085132.png]]
![[Pasted image 20250307085711.png]]
1st host id reserved for network id - 201.20.30.0
last id reserved - 201.20.30.255
limited broadcast - 255.255.255.255 (same organization)
direct - 201.20.30.255 (dusre network me broadcast)
![[Pasted image 20250307090317.png]]
![[Pasted image 20250307105655.png]]
![[Pasted image 20250307105705.png]]
![[Pasted image 20250307090556.png]]
![[Pasted image 20250307090625.png]]
![[Pasted image 20250307090653.png]]
![[Pasted image 20250307090800.png]]
![[Pasted image 20250307090831.png]]
![[Pasted image 20250307091245.png]]
![[Pasted image 20250307091851.png]]

ipv4 header
![[Pasted image 20250509132027.png]]
![[Pasted image 20250509132040.png]]

ipv6 header
![[Pasted image 20250509132109.png]]
![[Pasted image 20250509132200.png]]

![[Pasted image 20250509135106.png]]

| ✅ **Improvement Area**                | 🌐 **IPv4**                                                             | 🚀 **IPv6 Improvement**                                               |
| ------------------------------------- | ----------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **Address space**                     | 32-bit → ~4.3 billion addresses                                         | 128-bit → ~340 undecillion (3.4 ×10³⁸) addresses; virtually unlimited |
| **Address configuration**             | Manual config or DHCP required                                          | Autoconfiguration (stateless) via Neighbor Discovery                  |
| **Header simplicity**                 | Complex, variable header size (20–60 bytes)                             | Simplified, fixed 40-byte header → faster processing                  |
| **Security**                          | IPsec optional                                                          | IPsec built into protocol (mandatory support)                         |
| **NAT (Network Address Translation)** | Widely used to conserve addresses, complicates end-to-end communication | No NAT needed; end-to-end connectivity restored                       |
| **Multicast & anycast**               | Limited, not consistently supported                                     | Native, efficient support for multicast and anycast                   |
| **Mobility support**                  | Limited, complex (with Mobile IP)                                       | Designed with mobility in mind, more seamless                         |
| **QoS (Quality of Service)**          | Uses Type of Service (ToS), rarely used                                 | Uses Flow Label field → better QoS handling                           |
| **Fragmentation**                     | Done by routers                                                         | Done only by sender, routers no longer fragment → improved efficiency |
| **Extension & flexibility**           | Limited space for options                                               | Extension headers allow adding new features easily                    |

✅ **1. Built-in IPsec (Internet Protocol Security)**

- **IPv4:**  
    IPsec is optional; it was added later and is not always implemented or used.
    
- **IPv6:**  
    IPsec is mandatory — all IPv6 devices must support it in the protocol stack.
    
    → This enables:
    
    - Data confidentiality (encryption)
        
    - Data integrity (detection of tampering)
        
    - Authentication (verifying sender’s identity)
        

⚠ **Important:** While IPsec is required to be _available_ in IPv6, it is not automatically _enabled_. Admins still need to configure and manage it.

---

✅ **2. Simplified network design (no NAT)**

- **IPv4:**  
    Uses NAT (Network Address Translation) to deal with address shortages. NAT hides private networks, but:
    
    - Breaks true end-to-end encryption
        
    - Complicates IPsec and VPNs
        
    - Makes troubleshooting harder
        
- **IPv6:**  
    Has an enormous address space, so **no NAT is needed**.
    
    - Restores **end-to-end connectivity**
        
    - Allows simpler, more secure peer-to-peer communication
        
    - Makes IPsec easier to use
        

---

✅ **3. Improved neighbor discovery with secure options**

- IPv6 replaces ARP (Address Resolution Protocol) with **Neighbor Discovery Protocol (NDP)**.
    
- NDP can use **Secure Neighbor Discovery (SEND)** to prevent spoofing and certain local attacks.
    
- IPv4’s ARP is inherently insecure and easily spoofed.
    

---

✅ **4. Extension headers for better control**

- IPv6 allows **extension headers** for things like routing, security, and mobility.
    
- This modularity allows the network to implement **new security features** more easily in the future.

Distance Vector Routing
![[Pasted image 20250509135137.png]]

Count to infinity problem
![[Pasted image 20250509135345.png]]
![[Pasted image 20250509135529.png]]
![[Pasted image 20250509135611.png]]

Link State Routing Algo
![[Pasted image 20250509135406.png]]
![[Pasted image 20250509135837.png]]

![[Pasted image 20250510053006.png]]
![[Pasted image 20250510053015.png]]