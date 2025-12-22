

---

### **Q51**

**Question:** Python can run in both interactive mode and non-interactive [script] mode.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
Python is highly flexible in its execution:

* **Interactive Mode:** Allows you to type code line-by-line in the Python shell (REPL) and see immediate results. This is great for testing and debugging.
* **Script Mode:** Involves writing code into a file (e.g., `script.py`) and executing the entire file at once. This is the standard for building applications.

---

### **Q52**

**Question:** Switches can implement communication between homogeneous networks or communication between heterogeneous networks and isolate broadcast domains.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
There are two reasons this is "Wrong":

1. **Network Type:** Switches (Layer 2) typically connect **homogeneous** networks (e.g., Ethernet to Ethernet). Connecting **heterogeneous** networks (like Ethernet to Frame Relay or ATM) is a function of a **Router** (Layer 3).
2. **Broadcast Domains:** By default, switches **forward** broadcasts to all ports. Only **Routers** (or VLANs configured on a switch) can isolate or "break" a broadcast domain.

---

### **Q53**

**Question:** In STP, a non-root-bridge switch can have two root ports.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
In the Spanning Tree Protocol (STP), the rules for port selection are strict:

* **Root Bridge:** Has no root ports (all its ports are Designated).
* **Non-Root Bridge:** Must have **exactly one Root Port**. This is the port with the lowest path cost back to the Root Bridge. If multiple paths exist, STP chooses one and blocks the others to prevent loops.

---

### **Q54**

**Question:** In the WLAN network architecture, ACs can be connected in-path or off-path mode.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
An AC (Access Controller) can be deployed in two physical modes:

* **In-path (Direct):** All data traffic from the APs passes through the AC before going to the core network.
* **Off-path (Side-path/Bypass):** The AC only handles the management/control traffic (CAPWAP). The actual user data traffic bypasses the AC and goes directly into the network switches, reducing the AC's workload.

---

### **Q55**

**Question:** SNMP is a standard-based network management protocol... An SNMP NMS and SNMP agent communicate with each other through the TCP protocol.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
SNMP (Simple Network Management Protocol) primarily uses the **UDP** protocol for communication.

* **NMS to Agent:** UDP Port 161 (for queries like Get/Set).
* **Agent to NMS:** UDP Port 162 (for unsolicited Traps/Informs).
While some specific implementations can support TCP for security reasons, the standard and most common deployment is UDP.

---

### **Q56**

**Question:** After receiving a tagged frame from the peer device, an access port of a switch checks the VLAN ID of the frame. If the VLAN ID is the same as PVID of the port, the port accepts the frame.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
Access ports are designed for devices that do not understand tags (like PCs). However, if an access port receives a **tagged** frame:

1. It checks the tag's VLAN ID.
2. If the Tag ID matches the port's **PVID** (Port VLAN ID), it accepts the frame, strips the tag, and processes it.
3. If it doesn't match, the frame is discarded.

---

### **Q57**

**Question:** TFTP uses TCP to transfer files, and the default server port number is 21.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
This statement confuses **FTP** and **TFTP**:

* **FTP:** Uses **TCP** and port **21** for control.
* **TFTP (Trivial FTP):** Uses **UDP** and port **69**. It is a much simpler, connectionless protocol with no authentication or directory listing.

---

### **Q58**

**Question:** As every two nodes in a full-mesh network are connected using cables, each node requires a large number of physical ports and connection cables, resulting in relatively high costs.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
In a **Full-Mesh** topology, every device has a direct point-to-point link to every other device.

* For  nodes, the number of links required is .
* This provides the highest redundancy and reliability, but the cabling and port requirements grow exponentially, making it extremely expensive and difficult to scale.

---

### **Q59**

**Question:** WLAN technology enables transmission of information by radio waves over the air. Currently, the 2.6 GHz and 5 GHz frequency bands are used.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
The standard unlicensed frequency bands for Wi-Fi are **2.4 GHz** and **5 GHz**.

* **2.6 GHz** is typically a licensed band used for mobile cellular networks (like LTE/4G), not standard WLAN/Wi-Fi.

---

### **Q60**

**Question:** Segment routing (SR) can be deployed with or without controllers.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
Segment Routing is highly adaptable:

* **Without a Controller:** Routers use a distributed control plane (like OSPF or IS-IS with SR extensions) to calculate paths independently.
* **With a Controller:** A centralized SDN controller (like a PCE) can be used to manage traffic engineering and complex path calculations across the whole network.

---

