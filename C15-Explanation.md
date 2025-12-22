
---

### **Q1-C15**

**Question:** What is the level of the domain '.com' in the URL [www.huawei.com](https://www.huawei.com)?
**A.** Top-level domain
**B.** Second-level domain
**C.** Root domain
**D.** Host name
**Correct Answer: A**

**Explanation:**

The Domain Name System (DNS) is structured as a hierarchy:

* **Root Domain:** Represented by a dot (`.`) at the very end (usually hidden).
* **Top-Level Domain (TLD):** The suffix like **.com**, **.org**, or **.net**.
* **Second-Level Domain:** The specific name registered by an entity, such as **huawei** in `huawei.com`.
* **Host Name:** The specific service or machine, such as **www**.

---

### **Q2-C15**

**Question:** Which of the following messages is sent by a DHCP server to carry the IP address assigned to a client during DHCP interaction?
**A.** DHCP Offer
**B.** DHCP Discover
**C.** DHCP Ack
**D.** DHCP Request
**Correct Answer: A**

**Explanation:**

The DHCP process follows the **DORA** sequence:

1. **Discover:** The client broadcasts to find a server.
2. **Offer:** The server responds with an available IP address and configuration. (**Answer A**)
3. **Request:** The client asks to use that specific offered IP.
4. **Ack (Acknowledgment):** The server confirms the lease and the client starts using the IP.

---

### **Q3-C15**

**Question:** Which of the following is the default destination port number of the FTP control channel?
**A.** 20
**B.** 22
**C.** 23
**D.** 21
**Correct Answer: D**

**Explanation:**

FTP (File Transfer Protocol) is unique because it uses two separate "channels" (connections):

* **Control Channel (Port 21):** Used for sending commands (login, list files, delete).
* **Data Channel (Port 20):** Used for the actual transfer of file data.
* *Note: Port 22 is SSH/SFTP, and Port 23 is Telnet.*

---

### **Q4-C15**

**Question:** Which of the following parameters can be assigned by a DHCP server to a DHCP client? (Multiple Choice)
**A.** Local IP address
**B.** Mask
**C.** DNS server address
**D.** Gateway address
**Correct Answer: ABCD**

**Explanation:**

DHCP is designed to make a device fully "network-ready" without manual configuration. A DHCP server can provide:

* **IP Address and Subnet Mask:** Essential for Layer 3 communication.
* **Default Gateway:** So the device knows how to reach other networks.
* **DNS Servers:** So the device can resolve names (like https://www.google.com/search?q=google.com) to IPs.
* **Lease Time:** How long the device can keep the address.

---

### **Q5-C15**

**Question:** FTP works in active or passive mode. TCP port 20 is used in both modes.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

This is a tricky but important distinction:

* **Active Mode:** The server initiates the data connection from its **Port 20** to a random port on the client.
* **Passive Mode (PASV):** The client initiates the data connection to a **random high port** (above 1024) provided by the server.
In Passive mode, Port 20 is **not** used. This mode was created to solve issues where client-side firewalls would block the incoming connection from the server in Active mode.

---

