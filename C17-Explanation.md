

---

## 1. Network Troubleshooting Methodology

**Question:** Which of the following is the most efficient first step when troubleshooting a network connectivity issue?
**Correct Answer: A. Check the physical layer connectivity (cables, ports, and power).**

### Why A is correct:

The standard troubleshooting approach follows the **OSI Model** (usually Bottom-Up). Since Layer 1 (Physical) is the foundation, you must ensure cables are plugged in and ports are active before testing complex logic like IP routing or OSPF. Checking the simplest possible failure first saves time.

### Why the others are incorrect:

* **B (Reconfiguring OSPF):** You shouldn't change complex routing protocols until you've confirmed the hardware and basic IP addressing are functional.
* **C (Replacing the Router):** This is an expensive and time-consuming step that should only be taken after all software and configuration checks fail.

---

## 2. Using Tracert for Path Analysis

**Question:** What information does the `tracert` (or `traceroute`) command provide that the `ping` command does not?
**Correct Answer: B. The specific path (IP addresses of routers) data takes to reach the destination.**

### Why B is correct:

* **Ping** only tells you if the destination is "alive" (Reachability).
* **Tracert** shows you **every "hop" (router)** along the way. If a connection fails, `tracert` shows exactly which router in the path dropped the packet, allowing you to pinpoint the location of the failure.

---

## 3. High Availability (VRRP)

**Question:** Which protocol is used to provide gateway redundancy by allowing multiple routers to share a single virtual IP address?
**Correct Answer: C. VRRP (Virtual Router Redundancy Protocol)**

### Why C is correct:

**VRRP** groups two or more physical routers into one "Virtual Router." If the primary (Master) router fails, the Backup router takes over the Virtual IP address instantly. To the end-users (PCs), the "Default Gateway" never changes, ensuring uninterrupted internet access.

---

## 4. Troubleshooting "Request Timed Out"

**Question:** While pinging a host, you receive a "Request Timed Out" message. What are the possible causes?
**Correct Answer: A, B, and C**

### Why these are correct:

* **A:** The destination host might be powered off or disconnected.
* **B:** A firewall along the path (or on the destination host itself) might be blocking ICMP Echo Request packets.
* **C:** There might be a routing issue where the destination host does not have a "Return Path" to send the reply back to you.

---

## 5. Interpreting Interface Status

**Question:** If an interface status is "Physical UP" but "Protocol DOWN," what is the most likely issue?
**Correct Answer: B. A Layer 2 mismatch (such as incompatible encapsulation or STP blocking).**

### Why B is correct:

* **Physical UP:** Means the cable is good and there is an electrical signal.
* **Protocol DOWN:** Means the "handshake" at Layer 2 (Data Link) has failed. This usually happens if one side is using PPP while the other uses HDLC, or if STP has blocked the port to prevent a loop.

---

## 6. Network Documentation

**Question:** Maintaining an up-to-date network topology diagram and IP address scheme is essential for efficient O&M.
**Correct Answer: Right**

### Why "Right" is correct:

Without documentation, troubleshooting a complex network becomes "guesswork." A clear diagram allows an engineer to visualize the flow of data and quickly identify which devices are involved in a specific service, significantly reducing the Mean Time to Repair (MTTR).

---

