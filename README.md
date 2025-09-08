# 🖧 Applied Industrial Internet of Things  
## Configuration of Address Resolution Protocol (ARP)  

---

## 🎯 Aim  
To construct a simple Local Area Network (LAN) using Cisco Packet Tracer and understand the concept and operation of Address Resolution Protocol (ARP).

---

## 📝 Problem Statement  
In a LAN, devices communicate using IP addresses, but actual data transfer takes place via MAC (Media Access Control) addresses. The Address Resolution Protocol (ARP) is responsible for mapping an IP address to its corresponding MAC address.  

The objective is to:  
- Build a LAN topology with PCs connected through a switch.  
- Assign IP addresses to each PC.  
- Use **ping** and **arp -a** commands to observe ARP operation.  
- Inspect ARP packets in Simulation mode.  
- Verify how the switch builds its **MAC Address Table (CAM Table)**.  

---

## 📌 Scope of the Solution  
- Understand how ARP enables host-to-host communication.  
- Demonstrate ARP request and reply exchange.  
- Observe how switches dynamically learn MAC addresses.  
- Provide a reproducible simulation file and demo for learning and practice.  

---

## ⚙️ Required Components  

### Hardware (Simulated in Cisco PT)  
- 1 × Cisco 2960 Switch (8-port or 24-port)  
- 3 × PCs (PC0, PC1, PC2)  
- Copper Straight-Through LAN Cables  

### Software  
- Cisco Packet Tracer (any version ≥ 7.x)  
- GitHub (for uploading files and documentation)  

---

## 🖥️ Step-by-Step Procedure  

### 1) Create Topology  
- Place **3 PCs** and **1 Switch** in the workspace.  
- Connect each PC to the switch using **Copper Straight-Through** cables:  
  - PC0 → Switch Fa0/1  
  - PC1 → Switch Fa0/2  
  - PC2 → Switch Fa0/3   

---

### 2) Assign IP Addresses  
On each PC:  
- **PC0** → `192.168.1.2 / 255.255.255.0`  
- **PC1** → `192.168.1.3 / 255.255.255.0`  
- **PC2** → `192.168.1.4 / 255.255.255.0`  

---

### 3) Verify ARP Table Before Communication  
On PC0 → Desktop → Command Prompt:  
```bash
arp -a
