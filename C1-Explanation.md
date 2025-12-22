---
### **Q1-C1**

**Question:** What is the disadvantage of a tree network?
**A.** Nodes at higher layers will cause more serious network problems if they become faulty.
**B.** Tree networks are built by connecting star networks.
**C.** Tree networks are built by connecting bus networks.
**D.** Tree networks are highly scalable.
**Correct Answer: A**

**Explanation:**

A tree topology is hierarchical. It has a "root" node and subsequent layers of child nodes. Because the lower layers depend on the connectivity provided by the upper layers, a failure at the top (the root or a core switch) disconnects every single node beneath it. This is known as a **single point of failure** for the branches below.

**Why the others are incorrect:**

* **B and C:** These describe structural characteristics or advantages (how a tree is built by connecting star networks), not disadvantages.
* **D:** This is actually an **advantage**. Tree networks are considered highly scalable because you can easily add new "branches" (hubs/switches) to expand the network.

---

### **Q2-C1**

**Question:** Which functions does a firewall provide?
**A.** Network isolation
**B.** Security policies
**C.** Remote access
**D.** VPN
**E.** NAT
**Correct Answer: A, B, C, D, E (All of them)**

**Explanation:**

Modern "Next-Generation" Firewalls (NGFW) are multi-functional security appliances:

* **A and B (Isolation and Policies):** This is the core job of a firewall—segmenting a "Trusted" network (Internal) from an "Untrusted" one (Internet) using rules.
* **C and D (Remote Access and VPN):** Most enterprise firewalls act as VPN gateways, allowing remote employees to securely tunnel into the office network with encrypted data.
* **E (NAT):** Firewalls almost always perform Network Address Translation (NAT) to allow multiple devices on a private network to share a single public IP address.

---

### **Q3-C1**

**Question:** A star network is robust and therefore not prone to faults.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

While a star network is better than a "Bus" network (where one cable break kills everything), it has a critical vulnerability: the **Central Hub/Switch**.

* If a single peripheral cable fails, only one computer goes down.
* **However**, if the central switch fails, the **entire network** fails. Because the whole network relies on one central piece of hardware, it cannot be described as "not prone to faults."

---

### **Q4-C1**

**Question:** A router can break broadcast domains.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

In networking, a "Broadcast" is a message sent to every device on a segment (like a shout in a room).

* **Switches** forward broadcasts to every port; they create one large "Broadcast Domain."
* **Routers** do not forward Layer 2 broadcasts by default. When a router receives a broadcast, it stops it. This "breaks" the domain into smaller, more manageable pieces, preventing network congestion (broadcast storms).

---
