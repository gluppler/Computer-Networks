

---

## 1. The Three-Layer Hierarchical Model

**Question:** In a typical enterprise campus network, which layer is responsible for high-speed data switching and forms the backbone of the network?

**Correct Answer: A. Core Layer**

### Why A is correct:

Modern campus networks follow a structured three-layer design to ensure scalability and performance:

* **Access Layer:** Connects end-user devices (PCs, APs, IP phones) to the network. Its main job is entry and security (Port Security, VLAN assignment).
* **Aggregation Layer:** Acts as a bridge between the Access and Core layers. It performs policy-based routing, security filtering (ACLs), and summarizes routes to keep the Core lean.
* **Core Layer:** The "Backbone." It is designed for maximum speed and reliability. It should not perform complex filtering; its only job is to switch traffic between different parts of the network as fast as possible.

---

## 2. Gateway Placement

**Question:** Where is the "User Gateway" (VLANIF interface) typically configured in a small-to-medium enterprise network?

**Correct Answer: B. Aggregation Layer or Core Layer**

### Why B is correct:

In smaller networks, the **Core switch** often acts as the Layer 3 gateway for all VLANs. In larger networks, this duty is moved to the **Aggregation layer**. Placing the gateway here allows the switch to route traffic between local VLANs (East-West traffic) without sending every single packet up to the Core, reducing congestion.

---

## 3. Network Redundancy (Stacking)

**Question:** Which Huawei technology allows two or more physical switches to be managed as a single logical device to eliminate loops without using STP?

**Correct Answer: C. iStack / CSS**

### Why C is correct:

While STP prevents loops, it does so by blocking ports, which wastes bandwidth.

* **iStack (Intelligent Stack):** Used for fixed-configuration switches (Access/Aggregation).
* **CSS (Cluster Switch System):** Used for high-end chassis switches (Core).
By "stacking" switches, you create a single logical unit. You can then use **Eth-Trunk** across different physical switches, providing high availability and full bandwidth utilization simultaneously.

---

## 4. Egress Network Design

**Question:** What is the primary purpose of the "Egress" part of the campus network?

**Correct Answer: A. To provide connection to external networks (Internet or WAN).**

### Why A is correct:

The Egress is the "Exit/Entrance" of the network. This is where you typically find:

* **Firewalls:** To inspect incoming and outgoing traffic.
* **Routers:** To handle BGP/Static routing to the ISP.
* **NAT:** To translate private internal IPs to public external IPs.

---

## 5. Wireless Integration

**Question:** When deploying a WLAN in a large campus, which management mode is most commonly used for Access Points (APs)?

**Correct Answer: B. Fit AP + AC (Access Controller)**

### Why B is correct:

In a "Fit AP" architecture, the **AC** centrally manages the configurations, security, and radio frequencies of all APs. This allows for seamless roaming (walking from one building to another without losing Wi-Fi) and centralized firmware updates, which is impossible in "Fat AP" (standalone) mode.

---

## 6. The Project Lifecycle

**Question:** In network engineering, what is the correct order of the project lifecycle?

**Correct Answer: A. Planning -> Design -> Implementation -> O&M -> Optimization**

### Why A is correct:

Professional network construction follows a cycle:

1. **Planning:** Understanding the "Why" and "How Many."
2. **Design:** Creating the topology and IP scheme.
3. **Implementation:** Installing and configuring the gear.
4. **O&M (Operations & Maintenance):** Monitoring and fixing issues.
5. **Optimization:** Upgrading and improving performance based on data.

---

