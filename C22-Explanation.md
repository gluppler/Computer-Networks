
---

### **Q1-C22**

**Question:** To conserve IP addresses, what mask size is used for IP addresses on router-to-router connections on an enterprise network?
**A.** 28
**B.** 29
**C.** 30
**D.** 24
**Correct Answer: C**

**Explanation:**

Point-to-point links (router-to-router) only require two usable IP addresses (one for each interface).

* A **30-bit mask** () provides a total of 4 addresses: 1 Network ID, 2 Usable IPs, and 1 Broadcast address.
* This is the most efficient traditional way to prevent wasting addresses.
* *Note: In modern networks, /31 is also sometimes used, but /30 remains the standard answer for enterprise conservation in most certification exams.*

---

### **Q2-C22**

**Question:** On a campus network, which of the following functions can be enabled on access switches to prevent employees from accessing the unauthorized DHCP-enabled router?
**A.** IPSG
**B.** DHCP relay
**C.** DHCP snooping
**D.** Port security
**Correct Answer: C**

**Explanation:**

**DHCP Snooping** is a security feature that acts like a firewall between untrusted hosts and trusted DHCP servers.

1. It divides ports into **Trusted** (connected to legitimate servers) and **Untrusted** (connected to users).
2. If an "unauthorized" router sends a DHCP Offer on an untrusted port, the switch drops the packet. This prevents "Rogue DHCP" attacks where users get wrong gateway info.

---

### **Q3-C22**

**Question:** Which of the following technologies can be used on a campus network to improve network reliability? (Multiple Choice)
**A.** iStack
**B.** CSS
**C.** VRRP
**D.** Link aggregation
**Correct Answer: ABCD**

**Explanation:**

Each of these technologies provides a different "layer" of redundancy:

* **iStack / CSS:** Virtualizes multiple physical switches into one logical switch to simplify management and provide chassis-level redundancy.
* **VRRP:** Provides a virtual "gateway" IP so that if one router fails, another takes over without users losing internet access.
* **Link Aggregation (Eth-Trunk):** Protects against a single cable or port failure by bundling multiple links together.

---

### **Q4-C22**

**Question:** Which of the following are stages in the lifecycle of a campus network project? (Multiple Choice)
**A.** Planning and design
**B.** Deployment and implementation
**C.** Network O&M
**D.** Network optimization
**Correct Answer: ABCD**

**Explanation:**

A network is not just "built and forgotten." The standard lifecycle (PPDIOO or similar models) includes:

1. **Planning/Design:** Assessing requirements and drawing the architecture.
2. **Deployment:** Physical installation and configuration.
3. **O&M (Operation and Maintenance):** Monitoring and fixing daily issues.
4. **Optimization:** Upgrading and tuning performance based on usage patterns.

---

### **Q5-C22**

**Question:** Certain terminals, such as servers and printers, can be allocated fixed IP addresses.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Devices that provide services (like servers) or are shared resources (like printers) should have **Static (Fixed) IP addresses**.

* If a printer's IP changed via DHCP every day, users would constantly lose their connection to it.
* This can be done via manual configuration on the device or "DHCP Reservation" on the server.

---

