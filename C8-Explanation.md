

---

### **Q1-C8**

**Question:** What is the TPID value of an 802.1Q-tagged frame?
**A.** 0x0800
**B.** 0x8847
**C.** 0x8100
**D.** 0x0806
**Correct Answer: C**

**Explanation:**
The **TPID (Tag Protocol Identifier)** is a 16-bit field in an Ethernet frame that indicates that a VLAN tag (802.1Q) follows. The fixed value for this is **0x8100**.

* **0x0800** is for standard IPv4.
* **0x0806** is for ARP.
* **0x8847** is for MPLS unicast.

---

### **Q2-C8**

**Question:** Which of the following is a valid VLAN ID?
**A.** 0
**B.** 4095
**C.** 65536
**D.** 4094
**Correct Answer: D**

**Explanation:**
VLAN IDs are stored in a 12-bit field within the 802.1Q tag ().

* The range is **0 to 4095**.
* However, **0** and **4095** are reserved for system use.
* Therefore, the **usable** range for configuration is **1 to 4094**.

---

### **Q3-C8**

**Question:** Based on which of the following cannot VLANs be assigned?
**A.** Interface
**B.** MAC address
**C.** Subnet
**D.** Transport-layer protocol
**Correct Answer: D**

**Explanation:**
VLANs are typically assigned based on Layer 2 or Layer 3 information:

* **Interface-based (Most common):** The VLAN is tied to a physical port.
* **MAC-based:** The VLAN is assigned based on the source MAC address.
* **Subnet-based:** The VLAN is assigned based on the source IP subnet.
* **Protocol-based:** Assigned based on the Network Layer protocol (e.g., IPv4 vs IPv6).
There is no standard method for assigning VLANs based on **Transport-layer protocols** (TCP/UDP ports).

---

### **Q4-C8**

**Question:** Which of the following interfaces can process data frames carrying multiple VLAN tags? (Multiple Choice)
**A.** Access
**B.** Bridge
**C.** Trunk
**D.** Hybrid
**Correct Answer: CD**

**Explanation:**

* **Access (A):** Can only belong to one VLAN. It strips the tag when sending to a host and adds a specific tag when receiving.
* **Trunk (C):** Designed to carry traffic for multiple VLANs over a single link (usually between switches).
* **Hybrid (D):** A Huawei-specific type that combines features of Access and Trunk. It can allow multiple tagged VLANs and multiple untagged VLANs.

---

### **Q5-C8**

**Question:** An access interface cannot process VLAN-tagged data frames, and immediately discards them upon receipt.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
This is a common misconception. When an Access interface receives a tagged frame:

1. It checks if the **VLAN ID** in the tag matches its own **PVID** (Port Default VLAN ID).
2. If the tag **matches** the PVID, the interface **accepts** and processes the frame.
3. If the tag **does not match**, the frame is discarded.
Because it *can* process them if the IDs match, the statement "cannot process... immediately discards" is **Wrong**.

---

