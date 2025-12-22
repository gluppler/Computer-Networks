
---

### **Q1-C12**

**Question:** What is the default increment of ACL rule IDs?
**A.** 20
**B.** 15
**C.** 5
**D.** 10
**Correct Answer: C**

**Explanation:**
In Huawei VRP, ACL rules are identified by IDs (e.g., rule 5, rule 10). The **default increment is 5**.

* This gap allows administrators to insert new rules between existing ones (for example, inserting a rule with ID 7 between 5 and 10) without having to delete and recreate the entire list.
* This is crucial because ACLs are processed from top to bottom.

---

### **Q2-C12**

**Question:** What is the number range of advanced ACLs?
**A.** 4000-4999
**B.** 3000-3999
**C.** 2000-2999
**D.** 6000-6999
**Correct Answer: B**

**Explanation:**
Huawei classifies ACLs into specific number ranges based on their capabilities:

* **2000–2999: Basic ACLs** (Filters based only on Source IP).
* **3000–3999: Advanced ACLs** (Filters based on Source/Destination IP, Protocol, and Port numbers).
* **4000–4999: Layer 2 ACLs** (Filters based on Source/Destination MAC and Ethernet Type).

---

### **Q3-C12**

**Question:** If the number of an ACL is 4010, which of the following fields can the ACL match?
**A.** Source IP address
**B.** Source IP address and destination IP address
**C.** Source MAC address, destination MAC address, and Layer 2 protocol type
**D.** Packet header and offset
**Correct Answer: C**

**Explanation:**
As noted in Q2, the range **4000–4999** is reserved for **Layer 2 ACLs**. Unlike Basic or Advanced ACLs which look at Layer 3 (IP) and Layer 4 (Port) information, Layer 2 ACLs focus on the Ethernet frame header. They are used to permit or deny traffic based on physical hardware addresses (MAC) and the protocol type field in the frame.

---

### **Q4-C12**

**Question:** Which of the following packets can match the ACL rule: `rule 1 permit tcp source any destination 192.168.1.1 0.0.0.0 destination-port eq 80`? (Multiple Choice)
**A.** Source IP: 10.1.1.1; Dest IP: 192.168.1.2; Dest Port: 80; Protocol: TCP
**B.** Source IP: 10.1.1.1; Dest IP: 192.168.1.1; Dest Port: 80; Protocol: UDP
**C.** Source IP: 10.1.1.1; Dest IP: 192.168.1.1; Dest Port: 80; Protocol: TCP
**D.** Source IP: 10.0.0.1; Dest IP: 192.168.1.1; Dest Port: 80; Protocol: TCP
**Correct Answer: CD**

**Explanation:**
Let's break down the rule requirements:

1. **Protocol:** Must be **TCP**. (Eliminates B, which is UDP).
2. **Source:** `any` (Any source IP is fine).
3. **Destination IP:** `192.168.1.1 0.0.0.0` (Must be exactly 192.168.1.1. Eliminates A, which is 192.168.1.2).
4. **Destination Port:** `eq 80` (Must be exactly port 80).

* **C matches all:** TCP + 192.168.1.1 + Port 80.
* **D matches all:** TCP + 192.168.1.1 + Port 80 (Different source IP is allowed because of `source any`).


---

### **Q5-C12**

**Question:** An advanced ACL can match the source and destination port numbers of packets, enabling it to filter TCP packets with a specified destination port number.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**
This is one of the primary differences between Basic and Advanced ACLs.

* **Basic ACLs (2000-2999):** Can only check the Source IP address.
* **Advanced ACLs (3000-3999):** Have "deep" inspection capabilities. They can look into the Layer 4 header to identify the protocol (TCP, UDP, ICMP, etc.) and specific **Source and Destination Port numbers** (such as Port 80 for HTTP or Port 443 for HTTPS). This allows for granular traffic control, such as allowing web browsing while blocking FTP.

---

