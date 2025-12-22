

---

## 1. Advanced AAA Components

**Question:** Which component of AAA is responsible for determining the specific rights and resources a user can access after they have been successfully identified?

**Correct Answer: B. Authorization**

### Why B is correct:

The AAA framework is the "gatekeeper" of the network:

* **Authentication:** "Are you who you say you are?" (Check login/password).
* **Authorization:** "What are you allowed to do?" (Assign command levels, access to specific VLANs, or time limits).
* **Accounting:** "What did you do?" (Record start/stop times and data usage for auditing).

---

## 2. Principle of Least Privilege

**Question:** What is the core definition of the "Principle of Least Privilege" in network security management?

**Correct Answer: D. Users are granted only the minimum rights necessary to perform their specific job functions.**

### Why D is correct:

To minimize security risks, an administrator should never give a standard user "full access" to a router. For example, a junior engineer might be granted **Level 1** (Monitoring only) while a senior admin uses **Level 3** (Management/Configuration). This ensures that if an account is compromised, the potential damage is limited.

---

## 3. Remote vs. Local AAA

**Question:** What is a significant disadvantage of using a "Local" AAA implementation compared to a "Server-based" implementation?

**Correct Answer: C. Local implementation does not scale well in large networks.**

### Why C is correct:

* **Local AAA:** The usernames and passwords are stored directly on each router/switch. If you have 500 routers and an employee leaves, you must manually delete their account from 500 different devices.
* **Server-based (RADIUS/TACACS+):** All devices point to a central server. You delete the account once on the server, and access is instantly revoked across the entire network.

---

## 4. MAC Address and Port Security

**Question:** Which of the following statements about a MAC address is true?

**Correct Answer: A. It is 48 bits long and represented as 12 hexadecimal digits.**

### Why A is correct:

A MAC address is a physical "burned-in" address.

* **First 24 bits:** Organizationally Unique Identifier (OUI) assigned to the manufacturer (e.g., Huawei).
* **Last 24 bits:** Unique identifier for the specific network interface card (NIC).
In Chapter 19, we learn to use these addresses for **Port Security**—binding a specific MAC to a switch port so no other device can plug in and gain access.

---

## 5. Security Model Selection

**Question:** Which access control model is the strictest and typically used in military or mission-critical environments?

**Correct Answer: D. Mandatory Access Control (MAC)**

### Why D is correct:

There are different ways to manage access:

* **DAC (Discretionary):** The "owner" of the data decides who else can see it.
* **RBAC (Role-Based):** Access is based on your job title (e.g., "HR" or "Engineering").
* **MAC (Mandatory):** Access is based on security clearances and sensitivity labels. The system enforces the rules, and users cannot change them.

---
