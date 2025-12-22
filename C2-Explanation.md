

---

### **Q1-C2**

**Question:** The OSI reference model divides a network into seven layers. Which of the following lists the seven layers in the correct order, from bottom to top?
**A.** Physical, Data Link, Network, Transport, Session, Presentation, Application
**B.** Physical, Data Link, Network, Session, Transport, Presentation, Application
**C.** Physical, Data Link, Network, Transport, Presentation, Session, Application
**D.** Physical, Data Link, Transport, Network, Session, Presentation, Application
**Correct Answer: A**

**Explanation:**
The OSI model is a conceptual framework that standardizes network functions. The correct order from **Layer 1 (bottom)** to **Layer 7 (top)** is:

1. **Physical** (Cables, bits)
2. **Data Link** (Frames, MAC addresses)
3. **Network** (Packets, IP addresses)
4. **Transport** (Segments, TCP/UDP)
5. **Session** (Managing connections)
6. **Presentation** (Data format, encryption)
7. **Application** (Network services for software)

---

### **Q2-C2**

**Question:** Which of the following port numbers is used by Telnet?
**A.** 6
**B.** 23
**C.** 17
**D.** 21
**Correct Answer: B**

**Explanation:**
Port numbers identify specific services at the Transport Layer.

* **23: Telnet** (Remote terminal access, unencrypted).
* **21: FTP** (File Transfer Protocol).
* *Note: Port 6 and 17 are actually the protocol numbers for TCP and UDP, respectively, in the IP header, rather than standard application port numbers.*

---

### **Q3-C2**

**Question:** What are functions of the network layer? (Multiple Choice)
**A.** Provide logical addresses for network devices.
**B.** Set up connections between processes on hosts.
**C.** Send packets from source hosts to destination hosts.
**D.** Route and forward data packets.
**Correct Answer: ACD**

**Explanation:**
The Network Layer (Layer 3) is primarily about **routing**:

* It uses **logical addresses** (IP addresses) to identify devices (A).
* It determines the best path for **packets** to travel from source to destination (C, D).
* **Option B is incorrect** because setting up connections between "processes" (like browser to web server) is the responsibility of the **Transport Layer (Layer 4)** using port numbers.

---

### **Q4-C2**

**Question:** Which of the following statements are true about the layers in the OSI reference model? (Multiple Choice)
**A.** Application layer: provides network services for applications.
**B.** Session layer: establishes, manages, and terminates sessions.
**C.** Network layer: defines logical addresses for routers to determine paths.
**D.** Transport layer: implements data transmission and error detection.
**Correct Answer: ABCD**

**Explanation:**
All these statements accurately describe the primary responsibilities of the respective layers. The Transport Layer (D) is particularly important as it handles reliable (TCP) vs. unreliable (UDP) delivery and manages retransmission if data is lost.

---

### **Q5-C2**

**Question:** A MAC address is 48 bits (6 bytes) in length and consists of 12 hexadecimal digits.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
A MAC address is a hardware address. It is written in hexadecimal (e.g., `00-0C-29-4F-8B-3C`). Since each hex digit is 4 bits,  bits. The first 24 bits are the **OUI** (Manufacturer ID) and the last 24 are assigned by the vendor.

---

### **Q6-C2**

**Question:** An ARP Reply packet is broadcast so that all hosts can receive it.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
This is a common point of confusion:

* **ARP Request:** Is a **Broadcast** (sent to everyone) because the sender doesn't know who has the target IP.
* **ARP Reply:** Is a **Unicast** (sent directly back to the requester) because the responder now knows the requester's MAC address from the initial request.

---

### **Q7-C2**

**Question:** Common data link layer protocols include Ethernet, PPPoE, and PPP.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
The Data Link Layer (Layer 2) handles how data is placed on the physical medium. **Ethernet** is the standard for wired LANs, while **PPP** and **PPPoE** are commonly used for Point-to-Point wide area network (WAN) connections, like your home DSL or fiber link.

---

