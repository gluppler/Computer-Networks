
---

## 1. Routing Table Contents

**Question:** Which of the following fields is not included in the output of the `display ip routing-table` command?
**Correct Answer: B. AdvRouter**

### Why B is correct:

The standard Huawei IP routing table shows the parameters needed to forward a packet.

* **Destination/Mask:** The target network.
* **Proto:** The protocol that discovered the route (e.g., Static, OSPF).
* **Pre:** The preference (priority) of the protocol.
* **Cost:** The metric for the route.
* **NextHop:** The address of the next router.
* **Interface:** The local port used to reach the next hop.
**AdvRouter** (Advertising Router) is a field found in specific protocol databases (like the OSPF LSDB), but it is not a standard column in the general IP routing table.

---

## 2. Default Route Preference

**Question:** What is the default preference of static routes on Huawei devices?
**Correct Answer: C. 60**

### Why C is correct:

In Huawei’s VRP system, different routing sources are assigned a "Preference" value to determine which route is best when multiple protocols find the same path. A **lower** value means a **higher** priority.

* **Direct:** 0 (Highest priority).
* **OSPF:** 10.
* **Static:** **60**.
* **RIP:** 100.

---

## 3. The Longest Match Rule

**Question:** According to the longest match rule, which of the following routes will a data packet destined for `10.1.1.1` match?
**Correct Answer: B. 10.1.1.0/24**

### Why B is correct:

When a router’s table has multiple entries that could fit a destination IP, it chooses the most specific one—the one with the **longest subnet mask** (highest prefix length).

* `10.1.1.0/30` would be the longest, but if the destination is `10.1.1.1`, and you have options like `/16` and `/24`, the **`/24`** is more specific than the `/16`.
* *Note:* If a `/30` were present and matched the IP, it would beat the `/24`.

---

## 4. Link-State Routing Protocols

**Question:** Which of the following are link-state routing protocols?
**Correct Answer: A and D (OSPF and IS-IS)**

### Why A and D are correct:

Routing protocols are categorized by how they share information:

* **Link-State (OSPF, IS-IS):** These protocols build a complete map (topology table) of the entire network area before calculating the shortest path.
* **Distance-Vector (RIP):** These only know the "distance" (hops) and "vector" (direction) to a network, essentially relying on "rumors" from neighbors.
* **Static:** This is not a protocol at all, but a manually configured entry.

---

## 5. Static Route Configuration (True/False)

**Question:** The priority (preference) of static routes cannot be manually specified.
**Correct Answer: False (Wrong)**

### Why "False" is correct:

While the **default** preference is 60, administrators can manually change the preference of a static route to create "Floating Static Routes". This allows a static route to act as a backup that only appears in the routing table if the primary route (like OSPF) fails.

---

## 6. Default Route Usage

**Question:** Which of the following statements regarding the default route are true?
**Correct Answer: B and C**

### Why these are correct:

* **B:** If a packet's destination doesn't match any specific entry in the routing table, the router uses the **Default Route** as a "Gateway of Last Resort".
* **C:** In the routing table, a default route is represented as **`0.0.0.0/0`**.

### Why the others are incorrect:

* **A:** Default routes are not only manual; they can be generated and advertised dynamically by protocols like OSPF.
* **D:** A routing table does **not** have to contain a default route to function; without one, the router simply drops any packet it doesn't have a specific destination for.

---

