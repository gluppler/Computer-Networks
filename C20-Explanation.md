
---

### **Q1-C20**

**Question:** In the standard NFV architecture, which of the following modules is responsible for virtualization of the underlying hardware?
**A.** OSS
**B.** MANO
**C.** VNF
**D.** NFVI
**Correct Answer: D**

**Explanation:**

The **NFVI (Network Functions Virtualization Infrastructure)** is the foundation of the NFV model. It consists of the physical hardware (compute, storage, and network) and the **virtualization layer** (Hypervisor). This layer abstracts the physical resources and presents them as virtual resources to run the virtual functions.

* **VNF (Virtual Network Function):** The software-based application (like a virtual firewall).
* **MANO:** The management and orchestration layer.
* **OSS:** Operational Support Systems (the high-level business management).

---

### **Q2-C20**

**Question:** In the SDN architecture, which of the following interfaces is used for communication between the controller and an SDN switch?
**A.** RESTCONF interface
**B.** RESTful interface
**C.** Northbound interface
**D.** Southbound interface
**Correct Answer: D**

**Explanation:**

SDN uses a directional naming convention for its interfaces:

* **Southbound Interface (SBI):** Connects the **Controller to the physical/virtual switches** (the Data Plane). Common protocols here include OpenFlow and NETCONF.
* **Northbound Interface (NBI):** Connects the **Controller to applications** and business logic. This typically uses RESTful APIs.

---

### **Q3-C20**

**Question:** In the OpenFlow architecture, which of the following packets are sent from the controller to a switch? (Multiple Choice)
**A.** Controller-to-Switch
**B.** Symmetric
**C.** Switch-to-Controller
**D.** Asynchronous
**Correct Answer: AB**

**Explanation:**

The OpenFlow protocol defines three main categories of messages:

1. **Controller-to-Switch (A):** Initiated exclusively by the controller to manage or inspect the switch state.
2. **Symmetric (B):** Can be initiated by **either** the switch or the controller (e.g., Hello or Echo/Keepalive messages).
3. **Asynchronous:** Initiated by the **switch** to inform the controller of events (e.g., packet-in or port status changes).
Since both A and B can be sent from the controller to the switch, they are the correct choices.

---

### **Q4-C20**

**Question:** Which of the following are NFV features? (Multiple Choice)
**A.** Partition division
**B.** Isolation
**C.** Encapsulation
**D.** Hardware independence
**Correct Answer: ABCD**

**Explanation:**

NFV leverages standard IT virtualization features to transform networking:

* **Partitioning (A):** Multiple VNFs can share the same physical server.
* **Isolation (B):** VNFs on the same hardware are logically separated; a failure in one does not affect the others.
* **Encapsulation (C):** A VNF is essentially a file (VM/container), making it easy to move or copy.
* **Hardware Independence (D):** VNFs run on general-purpose "White Box" or COTS (Commercial Off-The-Shelf) hardware rather than proprietary appliances.

---

### **Q5-C20**

**Question:** An OpenFlow switch forwards packets based on the flow table, and matches the destination MAC and IP addresses and other fields in the packets.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Traditional switches use separate tables for MACs and IPs. In contrast, an **OpenFlow switch** uses one or more **Flow Tables**. Each entry in the table contains "Match Fields" that can include Layer 2 info (MACs, VLANs), Layer 3 info (IPs), and even Layer 4 info (TCP/UDP ports). This allows for highly granular control over how specific "flows" of traffic are handled.

---

