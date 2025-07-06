### **📌 README.md for Small Business Network Configuration**

````
# 🏢 Small Business Network Configuration 🚀  
This project demonstrates how to configure a **router, switch, and PCs** for a small business network using **Cisco Packet Tracer**.  

## 📌 Network Topology  
🔹 **1 Router (2811)**  
🔹 **1 Switch (2960)**  
🔹 **3 PCs (PC0, PC1, PC2)**  
🔹 **Straight-through cables for connections**  

### **🔗 Topology Overview**  
- **Router Fa0/0 ↔ Switch Fa0/4**  
- **Switch Fa0/1 ↔ PC0**  
- **Switch Fa0/2 ↔ PC1**  
- **Switch Fa0/3 ↔ PC2**  

## ⚙️ Configuration Details  
### **🔹 Router Configuration (R1)**
```
enable
configure terminal
interface fastEthernet 0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
````

* **IP Address:** `192.168.1.1/24` (Default Gateway for PCs)

### **🔹 Switch Configuration (S1)**

```
enable
configure terminal
interface fastEthernet 0/1
switchport mode access
switchport access vlan 1
exit

interface fastEthernet 0/2
switchport mode access
switchport access vlan 1
exit

interface fastEthernet 0/3
switchport mode access
switchport access vlan 1
exit

interface fastEthernet 0/4
switchport mode trunk
exit
```

* **Fa0/1, Fa0/2, Fa0/3 → Access mode (PC connections)**
* **Fa0/4 → Trunk mode (Router connection)**

### **🔹 DHCP Configuration on Router**

```
enable
configure terminal
ip dhcp excluded-address 192.168.1.1 192.168.1.10
ip dhcp pool BUSINESS
network 192.168.1.0 255.255.255.0
default-router 192.168.1.1
dns-server 8.8.8.8
exit
```

* **DHCP assigns IPs** dynamically from `192.168.1.11 - 192.168.1.254`

---

## 🔧 **How to Use This Project?**

1️⃣ **Download Cisco Packet Tracer** from [NetAcad](https://www.netacad.com/).
2️⃣ **Open the project file** in Packet Tracer.
3️⃣ **Test Connectivity** using the `ping` command:

```
ping 192.168.1.1
```

4️⃣ **Ensure PCs receive IPs via DHCP.**

---

## 📂 **Download Project File**

📥 [Small\_Business\_Network.pkt](https://github.com/idabeygunarathna/Small-Business-Network/tree/main)

---

## 🌟 **Key Features**

✅ **Router and Switch Configurations**
✅ **DHCP for Automatic IP Assignment**
✅ **Basic VLAN Setup**
✅ **Network Connectivity Verified**

---

## 🏆 **Connect with Me**

💼 **LinkedIn:** [https://www.linkedin.com/in/inishi-dinethma-852376264](#)
📧 **Email:** [Inishidinethma735@gmail.com](#)

---

🔗 **GitHub Repository:** [https://github.com/idabeygunarathna/Small-Business-Network](#)

\#Networking #CCNA #Cisco #PacketTracer #IT #Cybersecurity



