
---

### **Q1-C5**

**Question:** Which of the following fields is not included in the output of the `display ip routing-table` command?
**A.** Destination/Mask
**B.** Proto
**C.** Interface
**D.** AdvRouter
**Correct Answer: D**

**Explanation:**

When you run the `display ip routing-table` command on a Huawei VRP device, the brief output shows the fundamental information needed for packet forwarding:

* **Destination/Mask:** The target network and its prefix length.
* **Proto:** The protocol that learned the route (e.g., Direct, Static, OSPF).
* **Pre:** The preference (priority) of the route.
* **Cost:** The metric of the route.
* **Flags:** Status indicators (e.g., R for relay, D for download to FIB).
* **NextHop:** The IP address of the next router.
* **Interface:** The outbound physical or logical interface.

**AdvRouter** (Advertising Router) is a field found in specific protocol databases (like the OSPF LSDB) but is **not** part of the standard IP routing table's brief output.

---

### **Q2-C5**

**Question:** What is the default preference of static routes?
**A.** 150
**B.** 10
**C.** 60
**D.** 0
**Correct Answer: C**

**Explanation:**

Preference (also known as Administrative Distance) determines which protocol is "trusted" most when multiple protocols provide a path to the same destination. **Lower values are preferred.**

* **Direct:** 0 (Most trusted)
* **OSPF:** 10
* **Static:** **60**
* **RIP:** 100
* **BGP:** 255 (Least trusted)

---

### **Q3-C5**

**Question:** According to the longest match rule, which of the following routes will the data packet destined for 172.16.10.1 match?
**A.** 172.16.10.2/32
**B.** 172.16.10.0/24
**C.** 172.16.0.0/16
**D.** 172.17.10.0/24
**Correct Answer: B**

**Explanation:**

The **Longest Match Rule** states that if a packet matches multiple entries in the routing table, the router will choose the one with the **highest mask length** (the most specific route).

* **A:** Does not match (172.16.10.2 is a different host than 172.16.10.1).
* **B:** Matches. The first 24 bits (172.16.10) match perfectly.
* **C:** Matches. The first 16 bits (172.16) match.
* **Comparison:** Between B (/24) and C (/16), B is the "longer" match and is selected.
* **D:** Does not match (172.17 vs 172.16).

---

### **Q4-C5**

**Question:** Which of the following are link-state routing protocols? (Multiple Choice)
**A.** BGP
**B.** IS-IS
**C.** OSPF
**D.** Static route
**Correct Answer: BC**

**Explanation:**

Routing protocols are categorized by how they share information:

* **Link-State (B & C):** OSPF and IS-IS. These protocols share the entire "map" (topology) of the network. Every router calculates the best path independently using the SPF (Dijkstra) algorithm.
* **Distance-Vector:** RIP and BGP (BGP is technically Path-Vector). These protocols share their routing tables with neighbors ("routing by rumor").
* **Static:** Not a dynamic protocol at all; it is manually configured.

---

### **Q5-C5**

**Question:** The summary route of 172.16.1.0/24, 172.16.2.0/24, and 172.16.5.0/24 is 172.16.0.0/22.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

To summarize these routes, we look at the third octet in binary:

* 1: `0000 0001`
* 2: `0000 0010`
* 5: `0000 0101`

A **/22** mask means the first 22 bits must be identical. A /22 mask in the third octet covers a range of **4** (e.g., 0 to 3).

* 172.16.0.0/22 covers `172.16.0.0` to `172.16.3.255`.
Because **172.16.5.0** falls outside that range, `172.16.0.0/22` is **not** a valid summary for all three. You would need a **/21** (which covers 0-7) to include all three networks.

---

