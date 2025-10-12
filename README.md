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





**IP Address Tables**

<img width="1248" height="605" alt="Ipv4 table" src="https://github.com/user-attachments/assets/94a489ed-929c-48c1-a5a5-43df6a07b4ea" />


<img width="1140" height="718" alt="ipv6 table" src="https://github.com/user-attachments/assets/699edb25-d2d2-44b9-abbf-b5fcb566b02b" />




**VLAN Configuration**

I assigned each topology to a specific VLANs to provide logical segmentation and security isolation between different network areas.
This VLAN strategy ensures that devices within each topology can communicate efficiently while being isolated from other topologies, 
enhancing both security and network performance. The Star topology in the Lecture Room uses VLAN 5, the Ring topology in the Office 
uses VLAN 10, the Extended Star topology in the Science Building uses VLAN 15, the Mesh topology in the Computer Lab uses VLAN 20,
and the Bus topology in the Library uses VLAN 25. This logical separation prevents broadcast storms from propagating across the entire
network and allows for tailored security policies for each department's specific needs.Each switch maintains a complete VLAN database 
containing all five VLANs, but individual ports are assigned to specific VLANs based on their topology and location. This approach 
provides centralized VLAN management while maintaining logical segmentation.


**Router Configuration**

The router configuration implements a "router-on-a-stick" topology, where a single physical interface (GigabitEthernet0/0) is connected to a switch port configured in trunk mode, allowing it to carry traffic for multiple VLANs. The router interface is logically divided into subinterfaces, each assigned to a specific VLAN using 802.1Q tagging and serving as that VLAN's default gateway. With both IPv4 and IPv6 addresses assigned in an organized scheme, this setup provides dual-stack inter-VLAN routing, enabling seamless communication between the different logical networks across the single, shared physical link





**Services Implemented**


**HTTP Server**
- Web services for network management
- Accessible via both IPv4 and IPv6
- Basic web interface for monitoring
  


**DNS Server**

 - Dual-stack DNS resolution
 - Forward and reverse lookup zones
 - Supports both IPv4 and IPv6 queries



**Security Implementation**

**Basic Security Measures**

1.**Router Secutity**
 - Console password
 - Enable secret password
 - SSH/Telnet access restrictions


   

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




**IPv6 Subnetting Project Documentation**

**Project Overview**

This project demonstrates the configuration and subnetting of an IPv6 network using a router and four end devices.
The objective was to apply IPv6 subnetting to divide a  network address into smaller, manageable subnets for different departments.


  
**Base IPv6 Network**

**Original IPv6 Address**: 2001:2A1:BAD::/64
- This main network was subnetted into smaller subnets to accommodate different groups of devices.
  
**Subnetting Methodology**

**Subnet Allocation Strategy**
- **TUT Department**: Assigned the 11th subnet from the base address

- **NWU Department**: Assigned the 75th subnet from the base address


**Subnet Calculation Process**
The base address 2001:2A1:BAD::/64 was subdivided by borrowing additional bits from the host portion to create multiple /64 subnets.


**Network Topology**

<img width="1912" height="963" alt="TOPOLOGY PART 2" src="https://github.com/user-attachments/assets/dddf9f7b-69cc-4fec-9727-6ecedf53d258" />

**Router**: Acts as the gateway for both subnets and handles inter-subnet communication.

**Devices**: Four end PCs connected to 2 switches, then the two switches are connected to the router.

**Connections**:

- Two PCs under the TUT subnet

- Two PCs under the NWU subnet


**Implementation Steps**
- **Base Network Analysis**: Started with 2001:2A1:BAD::/64

- **Subnet Planning**: Determined departmental requirements

- **Subnet Allocation**:

   *TTU: 11th subnet → 2001:2A1:BAD::A::/64

   *NWU: 75th subnet → 2001:2A1:BAD:4A::/64

- **Device Configuration**: Assigned sequential IP addresses within each subnet

- **Routing Configuration**: Set up inter-subnet routing on the router



**Key Features**
- **Hierarchical Addressing**: Logical subnet allocation based on departmental needs

- **Scalable Design**: Easy to add more subnets for additional departments

- **Efficient Resource Utilization**: Proper IPv6 address space management


**Challenges Faced**

1. **IPv6 Subnetting Complexity**
Initially, determining the correct subnets from the main /64 address (2001:2A1:BAD::/64) was challenging.
It required careful calculation to correctly allocate the 11th subnet to the CSE network and the 75th subnet to the BBA network.
This step was crucial to ensure proper address segmentation and avoid overlapping subnets.

2. **Device Communication Setup**
After assigning subnets, devices in different IPv6 networks could not communicate initially.
This issue occurred because IPv6 routing was not yet enabled on the router.
To resolve it, I enabled IPv6 routing using the following command:

ipv6 unicast-routing
<img width="882" height="886" alt="part 2 ipv6 configuration command" src="https://github.com/user-attachments/assets/b5fd3a79-650b-4d67-a590-fd592b738568" />


**Testing**

<img width="875" height="827" alt="TESTING PART 2" src="https://github.com/user-attachments/assets/91728566-81c4-48bb-b68b-3ce1cfc5dc12" />


**Conclusion**

This project successfully demonstrated how to perform IPv6 subnetting and configure multiple subnets within a network.
By assigning different subnets to separate departments (CSE and BBA), the setup allowed for organized addressing and efficient inter-device communication.
