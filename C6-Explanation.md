
---

## 1. OSPF Router ID

**Question:** Which of the following statements about an OSPF router ID is false?

**Correct Answer: D. A router ID must be the IP address of an interface on the router.**

### Why D is correct (False Statement):

While it is common practice to use an interface IP as the Router ID (RID), it is not a requirement. The RID is simply a 32-bit number in dotted-decimal format. You can manually configure an RID (e.g., `1.1.1.1`) that does not correspond to any actual IP address configured on the router's physical or logical interfaces.

### Why the others are true:

* **A:** If no manual ID is set, the router will automatically select the highest IP address among its loopback interfaces.
* **B:** If no loopback exists, it picks the highest IP among its active physical interfaces.
* **C:** The RID is the unique name/identifier for a router within an OSPF "autonomous system."

---

## 2. OSPF Area 0

**Question:** In OSPF, Area 0 is the backbone area.

**Correct Answer: Right**

### Why "Right" is correct:

OSPF uses a two-tier hierarchical structure to ensure scalability. All non-backbone areas (Area 1, Area 2, etc.) must be physically or logically connected to **Area 0**. The backbone area is responsible for distributing routing information between all other areas.

---

## 3. OSPF Packet Types

**Question:** Which of the following are OSPF packet types?

**Correct Answer: A, B, C, D, E (All of them)**

### Why these are all correct:

OSPF uses five distinct message types to establish neighbor relationships and synchronize databases:

* **A (Hello):** Used to discover neighbors and maintain "keepalive" connectivity.
* **B (Database Description - DD):** Describes the contents of the LSDB to ensure neighbors are synchronized.
* **C (Link State Request - LSR):** Requests specific pieces of information from a neighbor.
* **D (Link State Update - LSU):** Carries the actual data (LSAs) to update a neighbor's database.
* **E (Link State Acknowledgment - LSAck):** Confirms that a packet was received.

---

## 4. DR and BDR in OSPF

**Question:** In an OSPF broadcast network, which of the following statements regarding the DR (Designated Router) and BDR (Backup Designated Router) are true?

**Correct Answer: A and C**

### Why these are correct:

* **A:** To reduce the number of OSPF adjacencies on a multi-access network (like Ethernet), all "DR Other" routers only form full adjacencies with the DR and the BDR, rather than with every single router on the segment.
* **C:** The BDR acts as a "hot standby." If the DR fails, the BDR immediately takes over the DR role to prevent network downtime.

### Why the others are incorrect:

* **B:** By default, the router with the **highest** priority (and then the highest RID) is elected, not the lowest.
* **D:** While the DR helps manage updates, it is not the *only* router that can send LSU packets; however, it is the central point for synchronizing the network segment.

---

## 5. OSPF Neighbor State (Full)

**Question:** When an OSPF router's state is "Full," it means the neighbor relationship has been successfully established and the databases are synchronized.

**Correct Answer: Right**

### Why "Right" is correct:

The OSPF adjacency process goes through several states (Down, Init, 2-Way, ExStart, Exchange, Loading). **Full** is the final state. Reaching "Full" indicates that the routers have finished exchanging all link-state information and their Link State Databases (LSDB) are identical.

---

