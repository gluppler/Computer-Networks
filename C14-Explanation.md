
---

### **Q1-C14**

**Question:** Which of the following NAT technologies can only use an interface address as the post-NAT public address?
**A.** Easy IP
**B.** NAT Server
**C.** Dynamic NAT
**D.** Static NAT
**Correct Answer: A**

**Explanation:**

**Easy IP** is a special form of NAPT (Network Address Port Translation). It is specifically designed for scenarios where the public IP address of the egress interface is assigned dynamically (e.g., via DHCP or PPPoE).

* Unlike other NAT types that require an "address pool," Easy IP directly uses the **current IP address of the interface** as the translation source.
* It is the most common NAT implementation for small-to-medium offices and home routers.

---

### **Q2-C14**

**Question:** Which of the following NAT technologies can be deployed on egress network devices to enable external users to access only a TCP port of an intranet server?
**A.** Static NAT
**B.** NAT Server
**C.** Dynamic NAT
**D.** NAPT
**Correct Answer: B**

**Explanation:**

**NAT Server** (also known as Port Forwarding or Static NAT with port mapping) allows you to map a specific public IP and port to an internal server's private IP and port.

* This is used when you want the outside world to "see" a service (like a Web Server on port 80) without exposing the entire server.
* By specifying the port, you maintain better security by only allowing traffic to that one specific TCP/UDP service.

---

### **Q3-C14**

**Question:** Which of the following are not translated by NAPT? (Multiple Choice)
**A.** Destination IP address
**B.** Source port number
**C.** Destination port number
**D.** Source IP address
**Correct Answer: AC**

**Explanation:**

When an internal user accesses the internet:

* **NAPT translates:** The **Source IP** (D) and the **Source Port** (B). It replaces the private IP with a public one and assigns a unique port number to keep track of the session.
* **NAPT does NOT translate:** The **Destination IP** (A) or the **Destination Port** (C). The router needs to keep these original so the packet actually reaches the intended server on the internet (e.g., Google's IP and port 443).

---

### **Q4-C14**

**Question:** Which of the following NAT technologies can be used to enable external users to proactively access an intranet server? (Multiple Choice)
**A.** Static NAT
**B.** NAT Server
**C.** NAPT
**D.** Easy IP
**Correct Answer: AB**

**Explanation:**

Most NAT types (Dynamic NAT, NAPT, Easy IP) are **unidirectional**—they only work if the internal host starts the conversation.

* **Static NAT (A):** Creates a permanent 1-to-1 mapping. An external user can type in the public IP, and it always points to the same internal host.
* **NAT Server (B):** Creates a static mapping for a specific service (IP + Port).
Because these mappings are fixed in the NAT table, external users can "proactively" (initiate first) reach the internal server.

---

### **Q5-C14**

**Question:** NAPT translates not only IP addresses but also port numbers to implement 1:N mappings between public and private addresses.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

This is the core definition of **NAPT** (Network Address Port Translation). By using the Layer 4 **Port Number** as an identifier, a single public IP address can support thousands of internal private hosts simultaneously. The router keeps a "NAT session table" to remember which unique port belongs to which internal PC.

---

