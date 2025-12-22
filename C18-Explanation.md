

---

### **Q1-C18**

**Question:** Which of the following packet types is used by SNMPv2c to proactively send traps to an NMS and requires a response from the NMS?
**A.** Inform
**B.** Trap
**C.** Response
**D.** Notification
**Correct Answer: A**

**Explanation:**

SNMP allows devices to alert the **NMS (Network Management System)** when an event occurs.

* **Trap:** The device sends an alert but does **not** expect or wait for an acknowledgment. It is "unreliable" because the packet could be lost and the device would never know.
* **Inform (Answer A):** Introduced in SNMPv2c, this is a "confirmed" notification. The NMS must send an acknowledgment back to the device. If the device doesn't receive the response, it will resend the Inform. This makes it much more reliable for critical alerts.

---

### **Q2-C18**

**Question:** Unlike SNMPv1, SNMPv2c uses which of the following packet types to query OIDs in batches?
**A.** Get-Request
**B.** Get-Next-Request
**C.** GetBulk
**D.** GetContinue
**Correct Answer: C**

**Explanation:**

SNMPv1 used `Get-Request` (get one value) and `Get-Next-Request` (walk through a table one-by-one). This was very slow for large tables (like a routing table).
**SNMPv2c** introduced the **GetBulk** operation. It allows the NMS to request a large block of data in a single packet, significantly reducing network overhead and speeding up the management process.

---

### **Q3-C18**

**Question:** Which of the following are attributes of managed devices defined in the MIB? (Multiple Choice)
**A.** Status of an object
**B.** Data type of an object
**C.** Access permission of an object
**D.** OID of an object
**Correct Answer: ABCD**

**Explanation:**

The **MIB (Management Information Base)** is like a structured dictionary or database for the device. Every object in the MIB has specific attributes:

* **OID (D):** The "address" of the object (e.g., `.1.3.6.1.2.1.1.1.0`).
* **Data Type (B):** What kind of info it is (Integer, String, Counter).
* **Access Permission (C):** Can it be read-only, read-write, or not accessible?
* **Status (A):** The current operational state or value of that specific object.

---

### **Q4-C18**

**Question:** Which of the following new security features that SNMPv3 provides over SNMPv1 and SNMPv2c? (Multiple Choice)
**A.** Digital signature technology can be used to verify the source of SNMP packets.
**B.** The MD5 algorithm is supported for user authentication.
**C.** DES is supported for data encryption.
**D.** RSA is supported for asymmetric data encryption.
**Correct Answer: BC**

**Explanation:**

SNMPv1 and v2c are insecure because they use "community strings" (passwords) sent in **plaintext**. SNMPv3 introduced a robust security model:

* **Authentication (B):** Uses algorithms like **MD5** or SHA to verify the user's identity.
* **Encryption (C):** Uses protocols like **DES** or AES to scramble the data so that even if intercepted, it cannot be read.
* *Note: While signatures and RSA exist in other security fields, standard SNMPv3 focuses on MD5/SHA and DES/AES.*

---

### **Q5-C18**

**Question:** Network devices enabled with SNMP run the agent process. The management process of an NMS interacts with the agent process through SNMP packets.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

This describes the standard **Manager-Agent architecture**:

1. **Agent:** Software running on the managed device (switch/router). It collects local data.
2. **Manager (NMS):** Central software that requests data from the agent or receives alerts (Traps/Informs) from it.
The communication between them is done entirely using standard SNMP packet formats.

---

