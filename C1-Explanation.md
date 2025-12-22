

---

### **Q1-C1**

**Question:** What is the disadvantage of a tree network?
**A.** Nodes at higher layers will cause more serious network problems if they become faulty.
**B.** The tree network uses a hierarchical star structure.
**C.** The tree network can quickly connect multiple star networks together.
**D.** It is easy to expand the network scale.
**Correct Answer: A**

**Explanation:**
A tree topology is essentially a hierarchy. While it is great for scalability (D) and organization (B), it creates a high level of dependency. If a "root" node or a high-level distribution switch fails, every node branching off from it loses connectivity. This is known as a **single point of failure** for all downstream branches.

---

### **Q2-C1**

**Question:** Which functions does a firewall provide?
**A.** Isolates networks of different security levels.
**B.** Uses security policies to implement access control.
**C.** Implements remote access.
**D.** Implements data encryption and VPN services.
**E.** Implements network address translation (NAT).
**Correct Answer: ABCDE**

**Explanation:**
Modern firewalls (especially Next-Generation Firewalls or NGFWs) are multi-functional security appliances:

* **Isolation & Access Control (A, B):** The core job of a firewall is to define "Trust" (Internal) and "Untrust" (External/Internet) zones and filter traffic between them.
* **Remote Access & VPN (C, D):** Firewalls often act as VPN gateways, allowing remote employees to securely connect to the office using encrypted tunnels.
* **NAT (E):** Firewalls typically perform NAT to hide internal private IP addresses behind a single public IP.

---

### **Q3-C1**

**Question:** A star network is robust and therefore not prone to faults.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
While a star network is better than a bus network (because one cable break only affects one PC), it has a major vulnerability: the **Central Node** (usually a switch or hub). If the central switch fails, the entire network goes down. Therefore, it is not "fault-proof."

---

### **Q4-C1**

**Question:** A router can break broadcast domains.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
By default, Layer 2 switches forward broadcast frames to every port in a VLAN. However, a router (Layer 3) does not forward broadcast traffic from one interface to another. This "breaks" or limits the broadcast traffic to a local segment, which improves network performance and security.

---

