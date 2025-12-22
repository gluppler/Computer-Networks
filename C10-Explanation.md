
---

### **Q1-C10**

**Question:** To implement inter-VLAN communication through sub-interfaces, which of the following commands needs to be configured for VLAN termination on the sub-interfaces?
**A.** `port default vlan vlan-id`
**B.** `port trunk pvid vlan-id`
**C.** `dot1q termination vid vlan-id`
**D.** `port link-type hybrid vlan-id`
**Correct Answer: C**

**Explanation:**

When using a router for inter-VLAN routing (Router-on-a-Stick), the router's physical interface is divided into logical sub-interfaces. Since the switch sends tagged traffic to the router, the router must know which VLAN tag corresponds to which sub-interface. The command **`dot1q termination vid vlan-id`** tells the router to:

1. Remove the 802.1Q tag from incoming frames of that specific VLAN.
2. Add the 802.1Q tag to outgoing frames sent from that sub-interface.

---

### **Q2-C10**

**Question:** Which of the following statements about a Layer 3 switch is false?
**A.** Layer 3 switch can forward packets only at Layer 3.
**B.** Layer 3 switch can route packets through VLANIF interfaces.
**C.** Layer 3 switch can forward packets at both Layer 2 and Layer 3.
**D.** Layer 3 switch can route packets through Layer 3 physical interfaces.
**Correct Answer: A**

**Explanation:**

Layer 3 switches are "multi-layer" devices. They possess the hardware (ASICs) to perform **wire-speed Layer 2 switching** (using MAC tables) and **Layer 3 routing** (using IP routing tables). Statement A is false because it ignores the switch's fundamental ability to perform standard Layer 2 switching within the same VLAN.

---

### **Q3-C10**

**Question:** Which of the following statements is false about routing on Layer 3 switches?
**A.** If a Layer 3 switch finds that the destination MAC address... is the MAC address of its VLANIF interface, it sends the data frame to its routing module...
**B.** If the routing module... finds that the destination IP address is not the IP address of a local interface... it looks up a routing entry...
**C.** Layer 3 switch forwards the packet to the next hop... without re-encapsulating the data frame.
**D.** When routing a packet at Layer 3, a Layer 3 switch replaces the source and destination MAC addresses...
**Correct Answer: C**

**Explanation:**

Statement C is **false** because every time a packet is routed (moved from one subnet/VLAN to another), the Layer 2 Ethernet header must be rebuilt. The switch **must re-encapsulate** the frame with a new Source MAC (the MAC of the switch's outgoing interface) and a new Destination MAC (the MAC of the next hop or the end host).

---

### **Q4-C10**

**Question:** If sub-interfaces are configured to implement inter-VLAN communication, which of the following interfaces should be configured to connect a switch to a router? (Multiple Choice)
**A.** Hybrid
**B.** Trunk
**C.** Bridge
**D.** Access
**Correct Answer: AB**

**Explanation:**

To support sub-interfaces on a router, the link between the switch and the router must be able to carry **tagged frames** from multiple VLANs.

* **Trunk (B):** The standard choice for carrying multiple tagged VLANs.
* **Hybrid (A):** A Huawei-specific port type that can also be configured to send and receive tagged traffic for multiple VLANs, making it a valid (though less common) alternative to a Trunk port.

---

### **Q5-C10**

**Question:** During Layer 3 communication, the source and destination MAC addresses of a packet are changed each time it passes through a Layer 3 device.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

IP addresses are end-to-end identifiers and generally do not change (unless NAT is used). However, MAC addresses are **local identifiers**. Each time a packet crosses a router (a Layer 3 device), the router strips the old Layer 2 header and adds a new one to get the packet to the next physical hop. Therefore, the MAC addresses are swapped at every router along the path.

---

