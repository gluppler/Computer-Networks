

---

## 1. Integrated Network Forwarding

**Question:** When a data packet travels from a source host to a destination host across multiple routers, which of the following is true?

**Correct Answer: B. The destination IP address remains the same, but the destination MAC address changes at each hop.**

### Why B is correct:

This is a core "Day in the Life of a Packet" concept:

* **IP Address (Layer 3):** Acts like a mailing address. It stays the same from the start to the end so the routers know the ultimate destination.
* **MAC Address (Layer 2):** Acts like a "delivery truck." It only gets the packet to the *next* router. Once it arrives, the router strips the old MAC and adds a new one to reach the next neighbor.

---

## 2. Default Route Application

**Question:** In a campus network, which device is the most appropriate place to configure a "Default Route" (0.0.0.0/0) pointing toward the ISP?

**Correct Answer: D. The Egress Router**

### Why D is correct:

Internal routers use specific routes (like OSPF) to find internal buildings or VLANs. However, the internal routers don't know the path to every website on the Internet. The **Egress Router** (at the network exit) is configured with a default route that essentially says: "If the destination isn't inside our company, send it out to the Internet Service Provider."

---

## 3. Troubleshooting with "Display" Commands

**Question:** You have configured OSPF, but the neighbor relationship is stuck in the "Exchange" state. Which command would you use first to investigate?

**Correct Answer: C. `display ospf peer**`

### Why C is correct:

In Huawei’s VRP system, `display` commands are your primary diagnostic tools.

* `display ospf peer` shows the current state of neighbors.
* If they are stuck, it might indicate an MTU mismatch or a problem with the Link State Database (LSDB) synchronization.

---

## 4. VLAN Routing: Sub-interfaces vs. VLANIF

**Question:** Which method of inter-VLAN routing is commonly referred to as "Router-on-a-Stick"?

**Correct Answer: A. Configuring sub-interfaces on a router with dot1q encapsulation.**

### Why A is correct:

In "Router-on-a-Stick," a single physical link between a switch and a router carries traffic for multiple VLANs. The router's physical port is divided into **logical sub-interfaces** (e.g., `G0/0/0.10`), each acting as the gateway for a specific VLAN.

---

## 5. Network Optimization: Link Aggregation

**Question:** To prevent a single point of failure and double the bandwidth between two switches, an engineer should use:

**Correct Answer: B. Eth-Trunk**

### Why B is correct:

By bundling two 1Gbps physical links into one **Eth-Trunk** logical link, you get:

1. **2Gbps of bandwidth.**
2. **Redundancy:** If one cable is cut, the traffic instantly switches to the other without the STP protocol having to recalculate, which prevents network downtime.

---

