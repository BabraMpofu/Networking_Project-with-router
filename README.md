**Network Topology Project Documentation**

**Project Overview**
This comprehensive networking project demonstrates the implementation of five fundamental network topologies along withan integrated hybrid topology.
The project features dual-stack IPv4/IPv6 configuration, VLAN segmentation, and basic security measures.

**Five Topologies**

1.**Bus Topology**
- Layout :Linear network where all devices share a single communication line.
- Key Features:
*Single backbone cable connecting all nodes
*Data travels in both directions but only one device can send at a time
*Cost-effective but single point of failure
            

2. **Mesh Topology**
- Layout : Fully connected network where each device connects to every other device.
- Key Features :
Multiple paths for data transmission
High cabling complexity and cost
High redundancy and reliability
  
3. **Star Topology**
- Layout: All devices connect to a cental switch.
- Key Features:
*Centralized management
*Easy to troubleshoot
*Single point of failure at the center

4. **Ring Topology**
- Layout : Each device connects to two others, forming a closed loop.
- Key Features:
 *Equal access to all devices
*Unidirectional or bidirectional data flow
*Token passing mechanism

5. **Extended Star Topology**
- Layout : Hierarchical star topology with multiple levels of switches.
- key Features:
*Multiple layers of hierarchy
*Scalable design
*Improved fault isolation

**Hybrid Topology**
-A hybrid topology combines all different network topologies together to create a more efficient and reliable network. 
It takes the best features from different designs and merges them into one superior network structure.

<img width="1913" height="957" alt="babra_Mpofu_Hybrid!!" src="https://github.com/user-attachments/assets/4fc0e084-7811-4fe0-8cd7-51933be793a5" />

Topology  	  |    Location	Gateway	IP Range	Subnet Mask	VLAN
Star	        |  Lecture room	192.168.1.1	192.168.1.2-192.168.1.6	255.255.255.0	5
Ring	       |   Office	192.168.2.1	192.168.2.2-192.168.2.5	255.255.255.0	10
Extended Star 	Science building	192.168.3.1	192.168.3.2-192.168.3.5	255.255.255.0	15
Mesh	          Computer lab	192.168.4.1	192.168.4.2-192.168.4.6	255.255.255.0	20
Bus         	  Library	192.168.5.1	192.168.5.2-192.168.5.5	255.255.255.0	25


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
*Forward and reverse lookup zones
*Forward and reverse lookup zones
*Supports both IPv4 and IPv6 queries

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





