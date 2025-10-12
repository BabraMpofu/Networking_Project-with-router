**Network Topology Project Documentation**

**Project Overview**

This comprehensive networking project demonstrates the implementation of five fundamental network topologies along withan integrated hybrid topology.
The project features dual-stack IPv4/IPv6 configuration, VLAN segmentation, and basic security measures.

**Five Topologies**

 1.**Bus Topology**
   - **Layout** :Linear network where all devices share a single communication line.

   - **Key Features**:
    
     *Single backbone cable connecting all nodes
    
     *Data travels in both directions but only one device can send at a time

     *Cost-effective but single point of failure

2.**Mesh Topology**
   - **Layout** : Fully connected network where each device connects to every other device.
    
   - **Key Features** :
    
      *Multiple paths for data transmission
    
      *High cabling complexity and cost
    
      *High redundancy and reliability

3.**Star Topology**
   - **Layout**: All devices connect to a cental switch.
  
   - **Key Features**:
  
      *Centralized management
  
      *Easy to troubleshoot
  
      *Single point of failure at the center

4.**Ring Topology**
   - **Layout** : Each device connects to two others, forming a closed loop.
      
   - **Key Features**:
      
       *Equal access to all devices
      
       *Unidirectional or bidirectional data flow
      
       *Token passing mechanism

5.**Extended Star Topology**
   - **Layout** : Hierarchical star topology with multiple levels of switches.
      
   - **key Features**:
      
       *Multiple layers of hierarchy
      
       *Scalable design
      
       *Improved fault isolation
     

**Hybrid Topology**
-A hybrid topology combines all different network topologies together to create a more efficient and reliable network. 
It takes the best features from different designs and merges them into one superior network structure.


<img width="1913" height="957" alt="babra_Mpofu_Hybrid!!" src="https://github.com/user-attachments/assets/4fc0e084-7811-4fe0-8cd7-51933be793a5" />


**IP Address Tables**

<img width="1248" height="605" alt="Ipv4 table" src="https://github.com/user-attachments/assets/94a489ed-929c-48c1-a5a5-43df6a07b4ea" />


<img width="1140" height="718" alt="ipv6 table" src="https://github.com/user-attachments/assets/699edb25-d2d2-44b9-abbf-b5fcb566b02b" />

**Router Configuration**


<img width="871" height="892" alt="routing" src="https://github.com/user-attachments/assets/901b15d4-fee7-4fb1-8708-42563a4d4b8e" />



**VLAN Configuration**

I assigned each topology to a specific VLANs to provide logical segmentation and security isolation between different network areas.
This VLAN strategy ensures that devices within each topology can communicate efficiently while being isolated from other topologies, 
enhancing both security and network performance. The Star topology in the Lecture Room uses VLAN 5, the Ring topology in the Office 
uses VLAN 10, the Extended Star topology in the Science Building uses VLAN 15, the Mesh topology in the Computer Lab uses VLAN 20,
and the Bus topology in the Library uses VLAN 25. This logical separation prevents broadcast storms from propagating across the entire
network and allows for tailored security policies for each department's specific needs.Each switch maintains a complete VLAN database 
containing all five VLANs, but individual ports are assigned to specific VLANs based on their topology and location. This approach 
provides centralized VLAN management while maintaining logical segmentation.


**VLAN Configuration (Example in a star topology)**

<img width="883" height="896" alt="configuration of a vlan" src="https://github.com/user-attachments/assets/94adbf2b-03aa-4a6d-870c-49f13e2c42c8" />


**VLAN Status in a star topology**

<img width="873" height="885" alt="VLAN CONFIGURED" src="https://github.com/user-attachments/assets/0ff99848-0fec-418b-9fe3-ab7201b925fc" />

**The Trunk Ports**: Carry multiple VLANs between switches and routers


<img width="857" height="316" alt="trunk" src="https://github.com/user-attachments/assets/08a665cc-e98f-4153-ae75-182614e1d609" />



**Services Implemented**


**HTTP Server**
- Web services for network management
- Accessible via both IPv4 and IPv6
- Basic web interface for monitoring
  
<img width="867" height="823" alt="HTTP" src="https://github.com/user-attachments/assets/c8f9cab8-c359-40f2-b96d-aa14d5321447" />


**DNS Server**

 - Dual-stack DNS resolution
 - Forward and reverse lookup zones
 - Supports both IPv4 and IPv6 queries

<img width="867" height="882" alt="DNS SERVER" src="https://github.com/user-attachments/assets/0ee8dcbf-ec1d-4900-9957-67fef768d073" />


**Security Implementation**

**Basic Security Measures**

1.**Router Secutity**
 - Console password
 - Enable secret password
 - SSH/Telnet access restrictions

<img width="882" height="890" alt="router password" src="https://github.com/user-attachments/assets/5f24fbe7-43d7-4561-ab69-799aa3814a6d" />
   

2.**Switch Security:**
- Central switch password protection
- VLAN access controls
- Port security configurations



**Implementation Challenges**

1.**IPv4 Subnet Mask Configuration**
  - **Problem**: Initially I used 255.255.0.0 (/16) subnet mask causing routing issues between VLANs
  - **Solution**: Changed to 255.255.255.0 (/24) for clearer subnet separation and better inter-VLAN routing
  - **Result**: Simplified configuration and improved cross-subnet communication

2. **Switch-Router Trunk Configuration**
  - **Problem**: Middle switch port was in access mode instead of trunk mode, blocking inter-VLAN traffic
  - **Solution**: Reconfigured the interface as a trunk port to carry multiple VLANs
  - **Result**: Restored proper communication between all VLANs and topologies


    
**Testing and verification**

**Pinging IPv4**

<img width="875" height="891" alt="pinging ipv4" src="https://github.com/user-attachments/assets/1c8b1f2a-e45c-4ea0-bfb0-be964af294ac" />


**Pinging IPv6**

<img width="871" height="885" alt="pinging IPV6" src="https://github.com/user-attachments/assets/04d7ca6c-046b-4af8-8488-1fcfc1a877ec" />



**Conclusion**

This project successfully demonstrates comprehensive network topology implementation with advanced features including dual-stack IP configuration, 
VLAN segmentation, and basic security measures. The hybrid topology shows effective integration of multiple network designs for optimal performance
and reliability in a real-world educational institution scenario.

