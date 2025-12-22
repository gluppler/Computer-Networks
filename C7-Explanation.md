
---

## 1. Switch Forwarding Behaviors

**Question:** Which of the following are the basic data frame forwarding behaviors of a layer 2 switch?
**Correct Answer: A, B, and C**

### Why A, B, and C are correct:

A Layer 2 switch makes decisions based on the MAC address table:

* **A (Flooding):** If the destination MAC is not in the table, or if it is a broadcast/multicast frame, the switch sends it out of all ports except the one it arrived on.
* **B (Forwarding):** If the destination MAC is known and associated with a specific port, the switch sends it directly to that port.
* **C (Discarding):** If the destination MAC is on the same port the frame arrived from (common in legacy hub connections), the switch drops the frame to prevent loops.

---

## 2. Default VLAN (PVID)

**Question:** By default, what is the default VLAN (PVID) for all interfaces on a Huawei switch?
**Correct Answer: A. 1**

### Why A is correct:

Out of the box, every Huawei switch is configured with **VLAN 1** as the default management VLAN. Every physical port is assigned a Port VLAN ID (PVID) of 1 until an administrator manually changes it.

---

## 3. Access Port Tagging Behavior

**Question:** When an Access interface receives a frame with a VLAN tag that matches its PVID, what does it do?
**Correct Answer: A. Strip the tag and forward the frame.**

### Why A is correct:

**Access ports** are designed to connect to end-user devices (PCs, printers) that do not understand VLAN tags.

1. The port checks if the tag matches its assigned PVID.
2. If it matches, it **removes (strips)** the tag before sending the raw Ethernet frame to the host.
3. This ensures the end-host receives a standard, readable frame.

---

## 4. Trunk Port Functionality

**Question:** Which of the following statements regarding Trunk interfaces are true?
**Correct Answer: B and C**

### Why these are correct:

* **B:** A Trunk port can carry traffic for **multiple VLANs** simultaneously, allowing different VLANs to communicate across multiple switches over a single physical link.
* **C:** When a frame is sent over a Trunk link, the switch adds a **VLAN tag** (802.1Q) so the receiving switch knows which VLAN the frame belongs to.

### Why the others are incorrect:

* **A:** Trunk ports are generally used to connect **switches to switches** or switches to routers, not directly to terminal hosts (PCs).
* **D:** Trunk ports do not strip tags by default for all VLANs; they only strip the tag for the **Native VLAN** (the PVID).

---

## 5. VLAN ID Range

**Question:** What is the maximum number of VLANs that can be defined in the IEEE 802.1Q standard?
**Correct Answer: B. 4094**

### Why B is correct:

The VLAN ID field in the 802.1Q header is **12 bits** long.

*  possible values.
* **VLAN 0** and **VLAN 4095** are reserved for system use.
* This leaves **4094** usable VLAN IDs (1–4094).

---

## 6. Layer 3 Switching (VLANIF)

**Question:** To enable communication between different VLANs, a Layer 3 device (like a Layer 3 switch or router) is required.
**Correct Answer: Right**

### Why "Right" is correct:

VLANs are Layer 2 broadcast domains. By design, traffic cannot move from one VLAN to another at Layer 2. To bridge the gap, you need a **Layer 3** device to route the packets. On a switch, this is typically done using a **VLANIF interface**, which acts as a virtual gateway for each VLAN.

---

