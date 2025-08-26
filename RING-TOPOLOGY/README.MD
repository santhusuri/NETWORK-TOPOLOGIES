# Ring Topology using Cisco Packet Tracer

## 📌 Objective
- Simulate a **Ring Topology** in Cisco Packet Tracer.  
- Connect multiple PCs in a circular path where each device connects to two others.  
- Assign static IP addresses and test connectivity using `ping`.

---

## 🏗️ Network Topology
![Ring Topology](topology.png)  
*(Replace `topology.png` with a screenshot of your Packet Tracer Ring Topology)*

---

## ⚙️ Devices Used
- 4 × PCs (PC0, PC1, PC2, PC3)  
- Copper Crossover Cables (PC-to-PC connections)  

---

## 🔧 Configuration Steps
1. **Drag and drop devices:**
   - Place 4 Switches in a ring formation.  
   - Place 4 PCs (one connected to each switch).  
2. **Connect devices:**
   - PC1 (Fa0) ↔ Switch1 (Fa0/1)  
   - PC2 (Fa0) ↔ Switch2 (Fa0/1)  
   - PC3 (Fa0) ↔ Switch3 (Fa0/1)  
   - PC4 (Fa0) ↔ Switch4 (Fa0/1)  

   - Switch1 (Fa0/2) ↔ Switch2 (Fa0/2)  
   - Switch2 (Fa0/3) ↔ Switch3 (Fa0/2)  
   - Switch3 (Fa0/3) ↔ Switch4 (Fa0/2)  
   - Switch4 (Fa0/3) ↔ Switch1 (Fa0/3) 

   - This forms a complete **loop** (ring).
   
3. **Assign IP Addresses (Desktop → IP Config):**
   - PC0: `192.168.1.2 / 255.255.255.0`
   - PC1: `192.168.1.3 / 255.255.255.0`
   - PC2: `192.168.1.4 / 255.255.255.0`
   - PC3: `192.168.1.5 / 255.255.255.0`
   - (No Default Gateway needed, no router in this setup).

---

## ✅ Verification
- From **PC0**, open Command Prompt and test:
  ```bash
  ping 192.168.1.3
  ping 192.168.1.4
  ping 192.168.1.5

---

## 📚 Learning Outcome

Understood how a Ring Topology works (each device connects to exactly 2 others).

Observed how data flows in one direction through the ring until it reaches the destination.

## 🌟 Advantages

Simple and cost-effective for small networks.

Predictable traffic flow.

## ❌ Disadvantages

Single point of failure: If one link breaks, the whole ring can fail.

Troubleshooting is harder compared to Star Topology.

Limited scalability (not suitable for large networks).

## 💡 Why Ring Topology is Rare Today

Replaced by Star and Mesh topologies that provide better reliability and redundancy.

Ring networks survive today mostly in legacy Token Ring or SONET/SDH (telecom rings) with dual-ring fault tolerance.
