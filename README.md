---
# Vic Modern Hotel Network Project

## Project Overview

This project involves the design and implementation of a network for Vic Modern Hotel using Cisco Packet Tracer. 
The hotel consists of three floors, each with multiple departments. 
The network design includes routers, switches, VLANs, WiFi networks, DHCP, OSPF routing, SSH configuration, and port security.

## Network Design Requirements

### Floor Layout and Departments
- **1st Floor**: Reception (VLAN 80), Store (VLAN 70), Logistics (VLAN 60)
- **2nd Floor**: Finance (VLAN 50), HR (VLAN 40), Sales/Marketing (VLAN 30)
- **3rd Floor**: Admin (VLAN 20), IT (VLAN 10)

### Routers and Interconnectivity
- Three routers represents 3 floors. 
- Routers connected using serial DCE cables with the following networks:
  - 10.10.10.0/30
  - 10.10.10.4/30
  - 10.10.10.8/30

### Switches
- One switch per floor.

### Wireless Networks
- Each floor has WiFi networks for laptops and phones.

### VLAN Configuration
- **1st Floor**:
  - Reception: VLAN 80, Network 192.168.8.0/24
  - Store: VLAN 70, Network 192.168.7.0/24
  - Logistics: VLAN 60, Network 192.168.6.0/24
- **2nd Floor**:
  - Finance: VLAN 50, Network 192.168.5.0/24
  - HR: VLAN 40, Network 192.168.4.0/24
  - Sales: VLAN 30, Network 192.168.3.0/24
- **3rd Floor**:
  - Admin: VLAN 20, Network 192.168.2.0/24
  - IT: VLAN 10, Network 192.168.9.0/24

### DHCP Configuration
- Each router is configured as the DHCP server for its respective VLANs.

### Routing Protocol
- OSPF is used to advertise routes between routers.

### Device Communication
- All devices should be able to communicate with each other.

### Remote Access
- SSH configured on all routers for remote login.
- Test-PC in IT department (port fa0/4) used for remote login testing.

### Port Security
- Port security on IT-dept switch to allow only Test-PC access on port fa0/4 using sticky method with violation mode of shutdown.

## Configuration Steps

### 1. Configure Routers:
1. **Assign IP Addresses to Serial Interfaces**
2. **Enable OSPF Routing**
3. **Configure DHCP**
4. **Configure SSH**

### 2. Configure Switches
1. **Assign VLANs**:
2. **Assign Ports to VLANs**: 

### 3. Configure Port Security
1. **Enable Port Security on IT-dept Switch**:

### 4. Configure WiFi Networks
1. **Setup Wireless Routers**:
    - Configure SSIDs and security settings for each floor.

### 5. Test Configurations
1. **Verify DHCP**:
    - Ensure all devices receive IP addresses dynamically.
2. **Test OSPF Routing**:
    - Check connectivity between different VLANs.
3. **SSH Access**:
    - Test SSH access from Test-PC to all routers.
4. **Port Security**:
    - Verify only Test-PC can access fa0/4 on IT-dept switch.

## Conclusion
This README outlines the essential steps and configurations required to set up the Vic Modern Hotel network.
