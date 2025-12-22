---
### **Q1-C4**

**Question:** Which of the following is a private IP address?
**A.** 192.169.16.1
**B.** 172.17.1.254
**C.** 239.0.0.8
**D.** 172.32.16.254
**Correct Answer: B**

---

### **Detailed Explanation**

To identify the correct answer, you must remember the three specific ranges reserved by **RFC 1918** for private internal networks. Any IP address falling outside these ranges is considered a Public address (routable on the internet) or a Multicast address.

#### **The Reserved Private IP Ranges:**

1. **Class A:** `10.0.0.0` to `10.255.255.255`
2. **Class B:** `172.16.0.0` to `172.31.255.255`
3. **Class C:** `192.168.0.0` to `192.168.255.255`

---

#### **Analysis of Options:**

* **A. 192.169.16.1:** This is **Public**. The private Class C range ends at 192.168.x.x. Since this is 169, it is outside the private range.
* **B. 172.17.1.254 (Correct):** This is **Private**. It falls within the Class B private range (`172.16.x.x` through `172.31.x.x`). 17 is between 16 and 31.
* **C. 239.0.0.8:** This is a **Multicast** address (Class D). Class D ranges from `224.0.0.0` to `239.255.255.255`.
* **D. 172.32.16.254:** This is **Public**. The private Class B range ends exactly at 172.**31**.x.x. Therefore, 172.32 is a public address.

---

### **Q2-C4**

**Question:** How many IP addresses are available in network segment 172.16.0.0/30?
**A.** 1
**B.** 4
**C.** 2
**D.** 8
**Correct Answer: C**

**Explanation:**

To find the number of **available** (usable) host addresses, we use the formula 2^n - 2, where n is the number of host bits.

1. A **/30** prefix means 30 bits are for the network, leaving **2 bits** for hosts (32 - 30 = 2).
2. Total addresses = 2² = 4.
3. We must subtract **2** (one for the Network ID `172.16.0.0` and one for the Broadcast address `172.16.0.3`).
4. Available host addresses = 4 - 2 = 2.

*Note: /30 subnets are commonly used for point-to-point links between two routers.*

---

### **Q3-C4**

**Question:** Which of the following ICMP packets is used to detect the connectivity between the source and destination IP addresses?
**A.** ICMP Redirect
**B.** ICMP Echo
**C.** ICMP port unreachable
**D.** ICMP host unreachable
**Correct Answer: B**

**Explanation:**
The `ping` utility uses **ICMP Echo** messages to test reachability.

* The source sends an **ICMP Echo Request**.
* The destination responds with an **ICMP Echo Reply**.
If the Echo Reply is received, connectivity is confirmed. Options C and D are "Destination Unreachable" error messages, and Option A is used by routers to inform a host of a better path, not to test connectivity.

---

### **Q4-C4**

**Question:** Which of the following IP addresses can be manually configured and used by host interfaces? (Multiple Choice)
**A.** 10.2.3.4
**B.** 127.0.0.1
**C.** 224.0.0.18
**D.** 192.168.100.254
**Correct Answer: AD**

**Explanation:**

* **A (10.2.3.4):** This is a standard Class A private unicast address. It is valid for a host.
* **B (127.0.0.1):** This is the **Loopback** address. It is reserved for internal testing within a device and cannot be assigned to a physical host interface.
* **C (224.0.0.18):** This is a **Multicast** address (Class D). These are used for sending data to a group and cannot be assigned as a unique IP to a host interface.
* **D (192.168.100.254):** This is a standard Class C private unicast address. It is valid for a host.

---

### **Q5-C4**

**Question:** The router discards packets with a TTL value of 0.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
The **TTL (Time to Live)** field is a mechanism to prevent packets from looping infinitely in a network. Every router that processes a packet decrements (subtracts 1) the TTL value. If a router receives a packet and the TTL becomes **0**, the router must discard the packet and typically sends an **ICMP Time Exceeded** message back to the source.

---

