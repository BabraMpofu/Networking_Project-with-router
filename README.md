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
            

2. **Mesh Topology**
Layout** : Fully connected network where each device connects to every other device.
**Key Features** :
-Multiple paths for data transmission
-High cabling complexity and cost
-High redundancy and reliability
  
4. **Star Topology**
**Layout**: All devices connect to a cental switch.
**Key Features**:
-Centralized management
-Easy to troubleshoot
-Single point of failure at the center

4. **Ring Topology**
**Layout** : Each device connects to two others, forming a closed loop.
**Key Features**:
-Equal access to all devices
-Unidirectional or bidirectional data flow
-Token passing mechanism

5. **Extended Star Topology**
**Layout** : Hierarchical star topology with multiple levels of switches.
**key Features**:
-Multiple layers of hierarchy
-Scalable design
-Improved fault isolation

**Hybrid Topology**
-A hybrid topology combines all different network topologies together to create a more efficient and reliable network. 
It takes the best features from different designs and merges them into one superior network structure.

<img width="1913" height="957" alt="babra_Mpofu_Hybrid!!" src="https://github.com/user-attachments/assets/4fc0e084-7811-4fe0-8cd7-51933be793a5" />

**IP Address Tables**

<img width="1248" height="605" alt="Ipv4 table" src="https://github.com/user-attachments/assets/94a489ed-929c-48c1-a5a5-43df6a07b4ea" />

<img width="1140" height="718" alt="ipv6 table" src="https://github.com/user-attachments/assets/699edb25-d2d2-44b9-abbf-b5fcb566b02b" />

**VLAN Segmentation**

I assigned each topology to a specific VLANs to provide logical segmentation and security isolation between different network areas.
This VLAN strategy ensures that devices within each topology can communicate efficiently while being isolated from other topologies, 
enhancing both security and network performance. The Star topology in the Lecture Room uses VLAN 5, the Ring topology in the Office 
uses VLAN 10, the Extended Star topology in the Science Building uses VLAN 15, the Mesh topology in the Computer Lab uses VLAN 20,
and the Bus topology in the Library uses VLAN 25. This logical separation prevents broadcast storms from propagating across the entire
network and allows for tailored security policies for each department's specific needs.

**Services Implemented**

**HTTP Server**
- Web services for network management
- Accessible via both IPv4 and IPv6
- Basic web interface for monitoring

**DNS Server**
- Dual-stack DNS resolution
-Forward and reverse lookup zones
-Forward and reverse lookup zones
-Supports both IPv4 and IPv6 queries

**Security Implementation**

**Basic Security Measures**
1.**Router Secutity**
-Console password
-Enable secret password
-SSH/Telnet access restrictions

2.**Switch Security:**
- Central switch password protection
- VLAN access controls
- Port security configurations

**Security Configuration**
**Router Password Configuration**

<img width="867" height="848" alt="PASWORD SECURITY FOR ROUTER" src="https://github.com/user-attachments/assets/20530f44-91f5-47c5-82eb-f0d0c71ce904" />

**Conclusion**
This project successfully demonstrates comprehensive network topology implementation with advanced features including dual-stack IP configuration, 
VLAN segmentation, and basic security measures. The hybrid topology shows effective integration of multiple network designs for optimal performance
and reliability in a real-world educational institution scenario.

