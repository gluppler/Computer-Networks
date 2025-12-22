
---

## 1. Troubleshooting "Input Errors" on an Interface

**Question:** When checking an interface with `display interface`, you see a high number of "Input Errors" and "CRC" errors. What is the most likely cause?

**Correct Answer: A. A faulty cable or electromagnetic interference.**

### Why A is correct:

**CRC (Cyclic Redundancy Check)** errors occur when a frame is corrupted during physical transmission. This is almost always a Layer 1 issue.

* **Bad Cabling:** A damaged copper wire or a dirty fiber connector.
* **Duplex Mismatch:** One side is set to "Half" while the other is "Full."
* **Interference:** The cable is running too close to high-voltage power lines.

---

## 2. OSPF Router ID Conflicts

**Question:** If two routers in the same OSPF area are manually configured with the same Router ID, what will happen?

**Correct Answer: B. The OSPF neighbor relationship will fail to form, or the routing table will be unstable.**

### Why B is correct:

The **Router ID (RID)** must be unique within an OSPF autonomous system. It acts as the "legal name" for the router. If two routers have the same name, the Link State Advertisements (LSAs) will conflict, and the Dijkstra algorithm will fail to calculate a stable shortest path.

---

## 3. Asymmetric Routing Issues

**Question:** What is a common symptom of "Asymmetric Routing" (where traffic goes out one path and returns through another) when a stateful firewall is present?

**Correct Answer: C. TCP connections are dropped even though both paths are physically up.**

### Why C is correct:

Firewalls are "stateful," meaning they remember the "SYN" packet going out. If the "SYN-ACK" return packet comes back through a *different* firewall or a different interface that hasn't seen the initial request, the firewall will view it as an illegal packet and drop it.

---

## 4. DHCP Exhaustion Attacks

**Question:** Which security feature should be enabled on a switch to prevent a malicious user from exhausting all available IP addresses in a DHCP pool?

**Correct Answer: B. DHCP Snooping**

### Why B is correct:

**DHCP Snooping** builds a binding table of valid MAC-to-IP mappings. It can also limit the rate of DHCP discovery packets. This prevents "DHCP Starvation" attacks where an attacker sends thousands of fake requests to "steal" all the IPs, leaving none for legitimate users.

---

## 5. STP "Root Bridge" Stability

**Question:** Why is it a "best practice" to manually configure the Core Switch with an STP priority of 0 or 4096?

**Correct Answer: D. To ensure the Core Switch is always the Root Bridge and prevent network topology shifts.**

### Why D is correct:

In STP, the switch with the **lowest priority** becomes the Root Bridge (the center of the tree). If you leave it at default (32768), a cheap access switch plugged in later might happen to have a lower MAC address and take over as the Root. This would force all network traffic to travel through the slow access switch, causing a massive performance drop.

---

## 6. Project Handover: The Configuration File

**Question:** Before completing a project, which command must be run to ensure the configuration is saved and will persist after a power failure?

**Correct Answer: A. save**

### Why A is correct:

Huawei VRP devices have two configuration files:

1. **Current-configuration:** Resides in RAM (temporary).
2. **Saved-configuration:** Resides in Flash/NVRAM (permanent).
If you don't run the `save` command, all your hard work disappears the moment the router is turned off.

---

