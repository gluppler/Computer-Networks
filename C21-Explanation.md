

---

## 1. BGP (Border Gateway Protocol) Basics

**Question:** Which routing protocol is specifically designed to exchange routing information between different Autonomous Systems (AS) on the Internet?

**Correct Answer: C. BGP**

### Why C is correct:

While OSPF and RIP are **IGPs** (Interior Gateway Protocols) used *inside* a company, **BGP** is the only **EGP** (Exterior Gateway Protocol) used to connect different organizations and ISPs. It is a "Path Vector" protocol that focuses on stability and policy control rather than just the shortest path.

---

## 2. VRRP Master Selection

**Question:** In a VRRP group, if two routers have the same priority, how is the Master router determined?

**Correct Answer: B. The router with the higher IP address on the interface becomes the Master.**

### Why B is correct:

VRRP (Virtual Router Redundancy Protocol) uses a priority system (default is 100).

* If priorities are different, the **highest priority** wins.
* If priorities are identical (a tie), the router with the **highest IP address** on the VRRP-enabled interface is elected as the Master.

---

## 3. Stack Priority and Master Election

**Question:** When configuring iStack (Stacking), what is the purpose of the "Stack Priority"?

**Correct Answer: A. To determine which physical switch will act as the Master (Management) switch for the entire stack.**

### Why A is correct:

In a stack, one switch must be the "boss" (Master) to handle the control plane. Higher priority values (default is 100, max is 255) ensure that the most powerful or preferred switch takes control of the stack management.

---

## 4. VXLAN Fundamentals

**Question:** What is a primary benefit of using VXLAN (Virtual Extensible LAN) in a modern Data Center?

**Correct Answer: D. It allows Layer 2 networks to be extended across a Layer 3 infrastructure.**

### Why D is correct:

Traditional VLANs are limited to 4,094 IDs and cannot easily cross routers. **VXLAN** wraps a Layer 2 Ethernet frame inside a Layer 3 UDP packet. This allows virtual machines to move between different physical servers in different subnets while staying on the same "virtual" Layer 2 network.

---

## 5. IPv6 Transition: Dual-Stack

**Question:** Which IPv6 transition technology allows a device to run both IPv4 and IPv6 protocol stacks simultaneously?

**Correct Answer: B. Dual-Stack**

### Why B is correct:

Dual-Stack is the most common transition method. Every interface on the router or PC is configured with both an IPv4 address and an IPv6 address. The device chooses which protocol to use based on the destination it is trying to reach.

---

## 6. Network Management: Telemetry

**Question:** Compared to traditional SNMP polling, what is the main advantage of "Telemetry" for network monitoring?

**Correct Answer: A. It pushes data in real-time, providing much higher granularity and speed.**

### Why A is correct:

* **SNMP** is "Pull": The NMS asks the device for data every 5 minutes. You might miss a 10-second traffic spike.
* **Telemetry** is "Push": The device streams data continuously as it happens. This allows for the "Instant Analysis" seen in systems like Huawei iMaster NCE.

---

