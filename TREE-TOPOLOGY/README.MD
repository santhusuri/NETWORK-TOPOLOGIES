# Tree Topology using Cisco Packet Tracer

## 📌 Objective
- Simulate a **Tree Topology (Hybrid Star-Bus)** in Cisco Packet Tracer.  
- Build multiple star networks connected to a central backbone switch.  
- Assign static IP addresses and test connectivity.  

---

## 🏗️ Network Topology
![Tree Topology](topology.png)  
*(Replace `topology.png` with a screenshot of your Packet Tracer Tree Topology)*  

---

## ⚙️ Devices Used
- 1 × Core Switch (acts as backbone)  
- 3 × Access Switches (distribution layer)  
- 6 × PCs (2 per access switch)  
- Copper Straight-Through Cables  

---

## 📋 IP Addressing Plan
We use a **single subnet** for simplicity (can extend to VLANs later):

| PC   | Connected Switch | IP Address     | Subnet Mask    | Gateway (if router added) |
|------|------------------|----------------|----------------|---------------------------|
| PC1  | Access Switch1   | 192.168.1.2    | 255.255.255.0  | 192.168.1.1               |
| PC2  | Access Switch1   | 192.168.1.3    | 255.255.255.0  | 192.168.1.1               |
| PC3  | Access Switch2   | 192.168.1.4    | 255.255.255.0  | 192.168.1.1               |
| PC4  | Access Switch2   | 192.168.1.5    | 255.255.255.0  | 192.168.1.1               |
| PC5  | Access Switch3   | 192.168.1.6    | 255.255.255.0  | 192.168.1.1               |
| PC6  | Access Switch3   | 192.168.1.7    | 255.255.255.0  | 192.168.1.1               |

*(A Router can be added for external connectivity, otherwise a single LAN is enough.)*  

---

## 🔧 Configuration Steps
1. **Drag and drop devices:**
   - Place 1 core switch, 3 access switches, and 6 PCs.  
2. **Connections:**
   - Core Switch ↔ Access Switch1  
   - Core Switch ↔ Access Switch2  
   - Core Switch ↔ Access Switch3  
   - Each Access Switch ↔ 2 PCs (via Straight-Through cables).  
3. **Assign IP addresses** to PCs as per table above.  

---

## ✅ Verification
- From **PC1**, ping all other PCs (PC2–PC6).  
- If a router is added, ping the router’s gateway IP.  
- All devices should communicate since they share the same network.  

---

## 📚 Learning Outcome
- Understood how a **Tree Topology** combines **Star and Bus**.  
- Learned hierarchical design (Core → Distribution → Access).  
- Realized backbone’s importance for connectivity.  

---

## 🌟 Advantages
- Scalable for large networks (expand star networks easily).  
- Hierarchical and structured design (used in campuses & enterprises).  
- Easy to manage each branch independently.  

---

## ❌ Disadvantages
- **Backbone dependency** — if the core switch fails, the entire network goes down.  
- More cabling than simple Star Topology.  
- Troubleshooting backbone issues can be complex.  

---

## 💡 Real-World Usage
- Campus networks (core switch in data center, access switches on each floor).  
- Large enterprises where hierarchy reduces congestion.  
- Schools/universities (departments connected via distribution switches).  

---
