
---

## 1. STP Port States

**Question:** Which of the following is not an STP port state?
**Correct Answer: B. Discarding**

### Why B is correct:

The standard **IEEE 802.1D (STP)** defines five specific states: Blocking, Listening, Learning, Forwarding, and Disabled. **Discarding** is a state used in **RSTP** (Rapid Spanning Tree Protocol) and **MSTP**, which combines the Blocking, Listening, and Disabled states into one. In original STP, it does not exist.

### Why the others are incorrect:

* **A, C, & D:** These are standard STP states. **Forwarding** sends data, **Learning** builds the MAC table but doesn't send data, and **Blocking** only listens for BPDUs to prevent loops.

---

## 2. Eth-Trunk (Link Aggregation) Benefits

**Question:** Which of the following are benefits of using Eth-Trunk?
**Correct Answer: A, B, and C**

### Why these are correct:

Eth-Trunk bundles multiple physical links into one logical link:

* **A (Increased Bandwidth):** By bundling links (e.g., four 1Gbps links), the total logical bandwidth increases (to 4Gbps).
* **B (Higher Reliability):** If one physical link in the bundle fails, the traffic automatically shifts to the remaining active links without the network going down.
* **C (Load Balancing):** Eth-Trunk distributes traffic across all active physical links in the bundle, preventing any single link from being overwhelmed.

---

## 3. STP Root Bridge Election

**Question:** In STP, the bridge with the largest Bridge ID is elected as the Root Bridge.
**Correct Answer: Wrong**

### Why "Wrong" is correct:

In STP, "lower is better." The election for the Root Bridge is based on the **lowest Bridge ID**. The Bridge ID consists of a priority (default 32768) and the switch's MAC address. The switch with the smallest numerical value becomes the "center" of the spanning tree.

---

## 4. Eth-Trunk Mode Selection

**Question:** Eth-Trunk can work in manual load balancing mode or LACP mode.
**Correct Answer: Right**

### Why "Right" is correct:

* **Manual Mode:** The administrator manually defines the links. It doesn't use a protocol to negotiate, which is simple but cannot detect certain link failures.
* **LACP Mode (Link Aggregation Control Protocol):** Uses the 802.3ad standard to dynamically negotiate and maintain the bundle. It is more advanced because it can detect if a link is "up" but not actually passing data correctly.

---

## 5. STP Path Cost

**Question:** What does STP use to determine the best path to the Root Bridge?
**Correct Answer: A. Path Cost**

### Why A is correct:

STP calculates the "Root Path Cost," which is the sum of the costs of all links leading to the Root Bridge. Cost is inversely proportional to link speed (e.g., a 100Mbps link has a higher cost than a 1Gbps link). STP always chooses the path with the **lowest total cost**.

### Why the others are incorrect:

* **B (Hop Count):** This is used by RIP, not STP.
* **C (IP Address):** STP operates at Layer 2 and does not care about IP addresses.
* **D (VLAN ID):** While MSTP uses VLANs, basic STP treats the entire physical broadcast domain as one unit regardless of VLANs.

---

## 6. LACP Active Link Selection

**Question:** In LACP mode, you can configure the maximum number of active links.
**Correct Answer: Right**

### Why "Right" is correct:

LACP allows for "M:N" backup. You might bundle 8 links but set the **maximum active links** to 4. The switch will use the 4 highest-priority links for data and keep the other 4 in "hot standby." If an active link fails, a standby link immediately takes its place.

---

