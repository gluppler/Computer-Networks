
---

## 1. ACL Matching Order

**Question:** When a router processes an ACL, in what order does it match the rules?
**Correct Answer: A. Based on the rule ID in ascending order.**

### Why A is correct:

By default, Huawei devices process ACL rules based on the **Rule ID** (usually increments of 5 or 10, such as 5, 10, 15). The router starts with the smallest ID and moves upward. Once a packet matches a rule, the action (Permit or Deny) is taken, and the router stops checking further rules for that packet.

### Why the others are incorrect:

* **B:** Rules are not processed in descending order; that would ignore the priority of the first-created rules.
* **C:** While many systems use "Top-to-Bottom," the technical mechanism in VRP is the numerical value of the Rule ID.
* **D:** Random matching would make security policies unpredictable and ineffective.

---

## 2. Basic ACL vs. Advanced ACL

**Question:** What is the range for a basic ACL?
**Correct Answer: B. 2000–2999**

### Why B is correct:

Huawei VRP categorizes ACLs by number to define their capabilities:

* **2000–2999:** **Basic ACLs.** These can only filter based on the **Source IP Address**.
* **3000–3999:** **Advanced ACLs.** These can filter based on Source IP, Destination IP, Protocol (TCP/UDP), and Port numbers.
* **4000–4999:** Layer 2 ACLs (based on MAC addresses).

---

## 3. NAT Functionality

**Question:** Which of the following are advantages of NAT?
**Correct Answer: A, B, and C**

### Why these are correct:

* **A (Address Conservation):** NAT allows hundreds of internal devices to use just one (or a few) public IP addresses, slowing the exhaustion of IPv4 addresses.
* **B (Security):** By hiding internal private IP addresses from the public internet, NAT provides a level of "security through obscurity."
* **C (Flexibility):** NAT allows internal networks to use any private addressing scheme without needing to change it if the ISP or public IP changes.

---

## 4. NAPT (Network Address Port Translation)

**Question:** NAPT allows multiple private IP addresses to be mapped to the same public IP address.
**Correct Answer: Right**

### Why "Right" is correct:

NAPT (also known as "PAT" or "NAT Overload") is the most common form of NAT. It uses **Layer 4 Port Numbers** to keep track of which internal device belongs to which session. This allows an almost unlimited number of internal hosts to "hide" behind a single public IP simultaneously.

---

## 5. NAT Server (Port Forwarding)

**Question:** The `nat server` command is used to allow external users to access an internal server.
**Correct Answer: Right**

### Why "Right" is correct:

Normally, NAT blocks unsolicited incoming traffic. To host a web server or mail server inside a private network, you must configure a **NAT Server** (Static NAT/Port Forwarding). This tells the router: "If traffic arrives on Public Port 80, send it specifically to Internal IP 192.168.1.10."

---

## 6. Wildcard Masks in ACLs

**Question:** In an ACL rule, what does a wildcard mask bit of "0" mean?
**Correct Answer: A. The corresponding bit must be checked (must match).**

### Why A is correct:

Wildcard masks are the opposite of subnet masks:

* **0:** "Check" — The bit in the IP address must exactly match the bit in the rule.
* **1:** "Ignore" — Any value in this bit position is acceptable.
* Example: `192.168.1.0 0.0.0.255` means the router checks the first three octets exactly but ignores the last one.

---
