
---

### **Q1-C13**

**Question:** Which of the following roles is not included in the common AAA network architecture?
**A.** User
**B.** AAA server
**C.** Network access server (NAS)
**D.** Portal server
**Correct Answer: D**

**Explanation:**

The standard AAA architecture consists of three core components:

1. **User:** The client/device requesting access.
2. **NAS (Network Access Server):** The gateway (like a switch, router, or AC) that intercepts user requests and communicates with the server.
3. **AAA Server:** The backend system (like a RADIUS or HWTACACS server) that stores credentials and makes decisions.
While a **Portal Server** is often used in web-based authentication (like hotel Wi-Fi), it is considered an external auxiliary component and is not one of the three fundamental pillars of the primary AAA architecture.

---

### **Q2-C13**

**Question:** What are the transport layer protocol and authentication port number used by RADIUS?
**A.** UDP, 1813
**B.** UDP, 1812
**C.** TCP, 1813
**D.** TCP, 1812
**Correct Answer: B**

**Explanation:**

RADIUS (Remote Authentication Dial-In User Service) is the most common open-standard AAA protocol.

* **Protocol:** It uses **UDP** for speed and efficiency.
* **Authentication Port:** **1812**.
* **Accounting Port:** **1813**.
(Note: Older versions of RADIUS sometimes used ports 1645 and 1646, but 1812/1813 are the modern RFC standards).

---

### **Q3-C13**

**Question:** Which of the following authorization modes is not supported by AAA?
**A.** Non-authorization
**B.** Local authorization
**C.** Mutual authorization
**D.** Remote authorization
**Correct Answer: C**

**Explanation:**

AAA supports several ways to grant permissions:

* **Local:** The NAS (router/switch) checks its own internal database.
* **Remote:** The NAS asks a RADIUS or HWTACACS server what the user is allowed to do.
* **None (Non-authorization):** Users are granted access without specific permission checks (rare but possible).
**Mutual authorization** is not a standard AAA mode; while "Mutual Authentication" exists in security (where both client and server prove identity), it is not a categorized authorization mode in this context.

---

### **Q4-C13**

**Question:** Which of the following concepts are involved in AAA? (Multiple Choice)
**A.** Accounting
**B.** Authentication
**C.** Authorization
**D.** Automation
**Correct Answer: ABC**

**Explanation:**

AAA stands for:

* **Authentication:** **Who** are you? (Verifying identity via username/password).
* **Authorization:** **What** can you do? (Granting permissions/privileges).
* **Accounting:** **How much** did you use? (Logging session time, data usage, and actions).
**Automation** is a separate network concept related to SDN and scripts, not a component of the AAA security framework.

---

### **Q5-C13**

**Question:** When receiving a user access request, the NAS determines the domain to which the user belongs based on the user name, and performs user management and control based on the AAA schemes configured for the domain.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Huawei devices use a **domain-based** management system. When a user logs in (e.g., `user1@huawei`), the NAS looks at the string after the `@` symbol to identify the domain. Each domain is mapped to specific AAA schemes (e.g., use RADIUS for authentication but Local for authorization). This allows a single device to handle different types of users (e.g., internal staff vs. guests) using different security rules.

---

