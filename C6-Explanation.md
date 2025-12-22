
---

### **Q1-C6**

**Question:** Which of the following packets are used by OSPF to discover and maintain neighbor relationships?
**A.** LSR
**B.** DD
**C.** Hello
**D.** LSU
**Correct Answer: C**

**Explanation:** OSPF uses five types of packets, but only the **Hello packet** is used for discovery and maintenance.

* **Hello:** Sent periodically (default every 10s on broadcast networks) to find neighbors and act as a "keepalive" to ensure they are still active.
* **DD (Database Description):** Used during the exchange phase to describe the contents of the database.
* **LSR (Link State Request):** Asks for specific missing data.
* **LSU (Link State Update):** Carries the actual routing information (LSAs).
* **LSAck:** Acknowledges receipt.

---

### **Q2-C6**

**Question:** By default, what are the OSPF cost values of a serial port working at 1.544 Mbit/s, FE interface, and GE interface, respectively?
**A.** 64, 10, 1
**B.** 640, 10, 1
**C.** 64, 10, 1
**D.** 64, 1, 1
**Correct Answer: D**

**Explanation:** OSPF calculates cost using the formula: .
In Huawei VRP, the default **Reference Bandwidth** is **100 Mbit/s**.

1. **Serial (1.544 Mbit/s):**  Integer value is **64**.
2. **Fast Ethernet (100 Mbit/s):** .
3. **Gigabit Ethernet (1000 Mbit/s):** . Since the minimum cost is 1, it becomes **1**.
*Note: This is why many engineers increase the reference bandwidth to 1000 or 10000 on modern networks so GE/10GE can have different costs.*

---

### **Q3-C6**

**Question:** Which of the following tables is used by OSPF to store link status information?
**A.** OSPF LSDB
**B.** OSPF peer table
**C.** OSPF routing table
**D.** OSPF adjaceny table
**Correct Answer: A**

**Explanation:** OSPF maintains three distinct databases/tables:

1. **Peer Table (Neighbor Table):** Lists discovered neighbors.
2. **LSDB (Link State Database):** This is the "map" of the entire area. It stores all received **LSAs (Link State Advertisements)**. This is where link status information lives.
3. **Routing Table:** The result of the SPF calculation (the best paths).

---

### **Q4-C6**

**Question:** Which of the following are OSPF network types? (Multiple Choice)
**A.** P2P
**B.** Broadcast
**C.** NBMA
**D.** P2MP
**Correct Answer: ABCD**

**Explanation:** OSPF adapts its behavior based on the underlying Layer 2 technology:

* **P2P (Point-to-Point):** Used for PPP or HDLC links. No DR/BDR election.
* **Broadcast:** Default for Ethernet. Requires **DR/BDR** election.
* **NBMA (Non-Broadcast Multi-Access):** Used for older technologies like Frame Relay or ATM. Neighbors must be manually configured.
* **P2MP (Point-to-Multipoint):** A variation used for star-topologies. No DR/BDR election.

---

### **Q5-C6**

**Question:** On an MA network, the final state of the OSPF neighbor relationship between DR others is 2-way.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:** On a Multi-Access (MA) network like Ethernet, routers only reach the **FULL** state with the **DR (Designated Router)** and the **BDR (Backup Designated Router)**.
Two "ordinary" routers (known as **DR Others**) do not need to synchronize their entire databases with each other. They stop their state machine at **2-way**, meaning they know each other exists but they rely on the DR to pass them the routing updates. This reduces the amount of OSPF traffic on the segment.

---

