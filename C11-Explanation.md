
---

## 1. SNMP Versions

**Question:** Which version of SNMP provides the highest level of security by supporting encryption and user-based authentication?
**Correct Answer: C. SNMPv3**

### Why C is correct:

SNMP (Simple Network Management Protocol) evolved specifically to address security flaws:

* **SNMPv1 & v2c:** Use "community strings" (plain-text passwords) which are easily intercepted.
* **SNMPv3:** Introduced the User-based Security Model (USM), which provides **authentication** (ensuring the message comes from a valid source) and **encryption** (protecting the data from being read by unauthorized parties).

### Why the others are incorrect:

* **A & B:** These are older versions that lack encryption, making them vulnerable to packet sniffing.
* **D (SNMPv4):** This version does not currently exist in the standard networking curriculum; SNMPv3 remains the modern standard.

---

## 2. IPv6 Address Structure

**Question:** An IPv6 address consists of how many bits?
**Correct Answer: D. 128**

### Why D is correct:

To solve the address exhaustion of the 32-bit IPv4 system, IPv6 was designed with a **128-bit** address space. This allows for  addresses (approximately 340 undecillion), which is enough to provide a massive number of unique IPs for every device on Earth for the foreseeable future.

---

## 3. IPv6 Address Simplification

**Question:** Which of the following is the correct compressed format for the IPv6 address `2001:0DB8:0000:0000:0000:0000:1234:5678`?
**Correct Answer: B. 2001:DB8::1234:5678**

### Why B is correct:

IPv6 has two primary compression rules:

1. **Leading Zero Compression:** You can remove leading zeros in any 16-bit block (e.g., `0DB8` becomes `DB8`).
2. **Double Colon Rule:** A contiguous sequence of blocks containing only zeros can be replaced by a single `::`. This can only be done **once** per address to avoid ambiguity.

---

## 4. SDN Architecture

**Question:** In the SDN (Software-Defined Networking) architecture, which plane is responsible for making decisions about where traffic is sent?
**Correct Answer: B. Control Plane**

### Why B is correct:

SDN decouples the "brains" of the network from the hardware:

* **Control Plane:** The centralized "Software Controller" that decides the path for traffic and creates the routing logic.
* **Forwarding/Data Plane:** The physical switches that simply follow the instructions given by the Control Plane to move packets.
* **Management Plane:** Used for administrative tasks and configuration.

---

## 5. IPv6 Neighbor Discovery (NDP)

**Question:** In IPv6, which protocol replaces the ARP protocol used in IPv4?
**Correct Answer: A. ICMPv6 (NDP)**

### Why A is correct:

IPv6 does not use broadcasts. Instead, it uses **Neighbor Discovery Protocol (NDP)**, which is built on top of **ICMPv6**. It uses "Neighbor Solicitation" and "Neighbor Advertisement" messages (sent via Multicast) to find the MAC address associated with an IPv6 address, performing the exact same function as ARP did in IPv4.

---

## 6. Cloud Computing and Virtualization

**Question:** NFV (Network Functions Virtualization) aims to replace traditional hardware appliances (like firewalls and load balancers) with software running on standard servers.
**Correct Answer: Right**

### Why "Right" is correct:

NFV is a key concept in modern data centers. Instead of buying a physical Cisco or Huawei firewall box, you run the firewall as a **Virtual Machine (VM)** on a high-powered generic server. This makes the network more flexible, easier to scale, and cheaper to maintain.

---

