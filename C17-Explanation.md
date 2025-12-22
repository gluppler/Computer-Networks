
---

### **Q1-C17**

**Question:** Which of the following packet types is used by PPPoE to terminate a session?
**A.** PADS
**B.** PADT
**C.** PADO
**D.** PADR
**Correct Answer: B**

**Explanation:**
PPPoE (Point-to-Point Protocol over Ethernet) has a specific termination phase.

* **PADT (PPPoE Active Discovery Terminate):** This packet can be sent by either the client or the server at any time after a session is established to indicate that the PPPoE session has been terminated.
* **Other packets:** PADO (Offer), PADR (Request), and PADS (Session-confirmation) are all part of the **Discovery Phase** used to establish the session, not end it.

---

### **Q2-C17**

**Question:** If a packet with unmatched parameters is received during LCP negotiation, which of the following packet types is used by PPP to respond to the packet?
**A.** Configure-Ack
**B.** Configure-Reject
**C.** Configure-Nak
**D.** Authenticate-Nak
**Correct Answer: C**

**Explanation:**
During the LCP (Link Control Protocol) phase, three types of responses exist for a Configuration Request:

* **Configure-Ack:** All parameters are recognized and accepted.
* **Configure-Reject:** Parameters are unrecognizable or not negotiable.
* **Configure-Nak:** The parameters are recognized but the **values** are unacceptable (unmatched). The "Nak" response includes a suggested value that the sender should use instead.

---

### **Q3-C17**

**Question:** Which of the following authentication protocols are supported by PPP? (Multiple Choice)
**A.** EAP-TLS
**B.** PAP
**C.** EAP-MD5
**D.** CHAP
**Correct Answer: BD**

**Explanation:**
The two primary authentication methods defined for PPP are:

* **PAP (Password Authentication Protocol):** A simple two-way handshake where the password is sent in **plaintext**.
* **CHAP (Challenge Handshake Authentication Protocol):** A more secure three-way handshake that uses a **MD5 hashing** algorithm so the password is never sent over the link.

---

### **Q4-C17**

**Question:** Which of the following packet types are used during PPP negotiation? (Multiple Choice)
**A.** LCP
**B.** PAP
**C.** CHAP
**D.** IPCP
**Correct Answer: ABCD**

**Explanation:**
A successful PPP session involves multiple layers of negotiation:

1. **LCP (Link Control Protocol):** Establishes, configures, and tests the physical link.
2. **Authentication (PAP/CHAP):** Optional phase to verify the identity of the peer.
3. **NCP (Network Control Protocol):** Configures different network layer protocols. **IPCP** (Internet Protocol Control Protocol) is the specific NCP used to negotiate IP addresses.

---

### **Q5-C17**

**Question:** During CHAP authentication, the password configured for a user is carried by PPP packets in plaintext.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**
This is the fundamental difference between PAP and CHAP.

* **PAP** sends the password in plaintext (unencrypted).
* **CHAP** uses a "Challenge" and "Response" mechanism. The password is used as a "key" to create an MD5 hash, but the **actual password is never transmitted**. This protects against "snooping" or "man-in-the-middle" attacks on the WAN link.

---

