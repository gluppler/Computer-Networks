
---

## 1. AAA Fundamentals

**Question:** What does the acronym AAA stand for in network security?

**Correct Answer: B. Authentication, Authorization, and Accounting**

### Why B is correct:

AAA is a framework used to control access to computer resources and enforce policies:

* **Authentication:** Verifying **who** the user is (e.g., username and password).
* **Authorization:** Determining **what** the user is allowed to do (e.g., commands they can run).
* **Accounting:** Measuring the resources the user consumes (e.g., **how long** they were logged in) for auditing.

---

## 2. Firewall Security Zones

**Question:** On a Huawei firewall, which of the following zones has the highest default security level?

**Correct Answer: A. Trust**

### Why A is correct:

Firewalls use security levels (0–100) to define trust:

* **Trust (Level 85):** Usually reserved for the internal, protected network.
* **DMZ (Level 50):** The "Demilitarized Zone" for public-facing servers.
* **Untrust (Level 5):** Usually represents the Internet or external networks.
* **Local (Level 100):** Refers to the firewall itself; it is the most secure zone.

---

## 3. Security Policy Matching

**Question:** When a firewall receives a packet, how does it match it against security policies?

**Correct Answer: B. It matches policies one by one from top to bottom.**

### Why B is correct:

Like ACLs, firewall security policies are processed sequentially. The device starts at the top of the list. Once a packet matches the criteria of a policy (Source/Destination Zone, IP, Port), the action (Permit or Deny) is taken immediately, and no further policies are checked.

---

## 4. Port Security

**Question:** Which feature can be used on a switch to prevent unauthorized devices from connecting to a specific port based on their MAC address?

**Correct Answer: C. Port Security**

### Why C is correct:

Port Security allows an administrator to limit the number of MAC addresses on a port or bind specific MAC addresses to a port. If an unauthorized device (with a different MAC) is plugged in, the switch can automatically shut down the port or discard the traffic.

---

## 5. Security Threats: DDoS

**Question:** What is the primary goal of a Distributed Denial of Service (DDoS) attack?

**Correct Answer: D. To exhaust the target's resources and make services unavailable.**

### Why D is correct:

A DDoS attack uses a large number of compromised systems (a "botnet") to flood a target with massive amounts of traffic. The goal is not to steal data, but to crash the server or clog the network so legitimate users cannot access the service.

---

## 6. VPN: Encryption and Integrity

**Question:** Which of the following is a key benefit of using a VPN (Virtual Private Network)?

**Correct Answer: A, B, and C**

### Why these are correct:

* **A (Confidentiality):** VPNs use **Encryption** to ensure that if data is intercepted, it cannot be read.
* **B (Integrity):** They use hashing to ensure that the data has not been **tampered** with during transmission.
* **C (Authentication):** They ensure that both ends of the "tunnel" are who they claim to be before allowing traffic.

---

