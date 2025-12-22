# HCIA-Datacom Mock Exam Questions

This document displays all mock exam questions (PNG images) organized by question type in numerical order.

## Directory Structure

- **Huawei-Single/**: Single-choice questions (Q1-Q30)
- **Huawei-Multi/**: Multiple-choice questions (Q31-Q50)
- **Huawei-TF/**: True/False questions (Q51-Q60)

**Total Questions:** 60

---

## Single-Choice Questions (Q1-Q30)

**Location:** `Huawei-Single/`

### Q1.png
![Q1](Huawei-Single/Q1.png)

---

### Q2.png
![Q2](Huawei-Single/Q2.png)

---

### Q3.png
![Q3](Huawei-Single/Q3.png)

---

### Q4.png
![Q4](Huawei-Single/Q4.png)

---

### Q5.png
![Q5](Huawei-Single/Q5.png)

---

### Q6.png
![Q6](Huawei-Single/Q6.png)

---

### Q7.png
![Q7](Huawei-Single/Q7.png)

---

### Q8.png
![Q8](Huawei-Single/Q8.png)

---

### Q9.png
![Q9](Huawei-Single/Q9.png)

---

### Q10.png
![Q10](Huawei-Single/Q10.png)

---

### Q11.png
![Q11](Huawei-Single/Q11.png)

---

### Q12.png
![Q12](Huawei-Single/Q12.png)

---

### Q13.png
![Q13](Huawei-Single/Q13.png)

---

### Q14.png
![Q14](Huawei-Single/Q14.png)

---

### Q15.png
![Q15](Huawei-Single/Q15.png)

---

### Q16.png
![Q16](Huawei-Single/Q16.png)

---

### Q17.png
![Q17](Huawei-Single/Q17.png)

---

### Q18.png
![Q18](Huawei-Single/Q18.png)

---

### Q19.png
![Q19](Huawei-Single/Q19.png)

---

### Q20.png
![Q20](Huawei-Single/Q20.png)

---

### Q21.png
![Q21](Huawei-Single/Q21.png)

---

### Q22.png
![Q22](Huawei-Single/Q22.png)

---

### Q23.png
![Q23](Huawei-Single/Q23.png)

---

### Q24.png
![Q24](Huawei-Single/Q24.png)

---

### Q25.png
![Q25](Huawei-Single/Q25.png)

---

### Q26.png
![Q26](Huawei-Single/Q26.png)

---

### Q27.png
![Q27](Huawei-Single/Q27.png)

---

### Q28.png
![Q28](Huawei-Single/Q28.png)

---

### Q29.png
![Q29](Huawei-Single/Q29.png)

---

### Q30.png
![Q30](Huawei-Single/Q30.png)

**Total Single-Choice Questions:** 30

---

## Multiple-Choice Questions (Q31-Q50)

**Location:** `Huawei-Multi/`

### Q31.png
![Q31](Huawei-Multi/Q31.png)

#### Explanation

**Question:** In contrast with SNMPv1, which of the following operations are newly added to SNMPv2c?
**A.** GetNextRequest
**B.** SetRequest
**C.** GetBulkRequest
**D.** InformRequest
**Correct Answer: CD**

**Explanation:**

SNMPv2c introduced two major enhancements to efficiency and reliability:

* **GetBulkRequest (C):** Allows a manager to retrieve large amounts of data (like an entire routing table) in a single response, rather than querying each row individually.
* **InformRequest (D):** Unlike a "Trap" (which is fire-and-forget), an "Inform" requires the NMS to send an acknowledgment. This makes event reporting reliable.

---

### Q32.png
![Q32](Huawei-Multi/Q32.png)

#### Explanation

**Question:** ACLs are used to match and distinguish packets. Which of the following information can be used to define ACL rules?
**A.** VLAN ID
**B.** Protocol type of Ethernet frames
**C.** Source and destination MAC addresses
**D.** Source and destination IP addresses of IPv4 packets
**Correct Answer: ABCD**

**Explanation:**

Huawei devices support different types of ACLs that can look at different headers:

* **Basic/Advanced ACLs (D):** Use IP addresses.
* **Layer 2 ACLs (A, B, C):** Use MAC addresses, Ethernet types, and VLAN IDs to filter traffic at the Data Link layer.

---

### Q33.png
![Q33](Huawei-Multi/Q33.png)

#### Explanation

**Question:** Refer to the configuration on VTY user interface 0. When a user logs in through VTY 0, which of the following are true?
`[~HUAWEI-ui-vty0] User privilege level 2`
**A.** Use debugging commands.
**B.** Use ping and tracert.
**C.** Use some display commands.
**D.** Use service configuration commands (routing).
**Correct Answer: BCD**

**Explanation:**

Huawei VRP uses a 16-level privilege system (0-15), summarized into four functional categories:

* **Level 0 (Visit):** Basic tools (ping, tracert).
* **Level 1 (Monitoring):** Display commands.
* **Level 2 (Configuration):** Service configuration commands (routing, interface setup). **(Answer BCD)**
* **Level 3+ (Management):** System maintenance and debugging. **(Answer A is False as it requires Level 3)**

---

### Q34.png
![Q34](Huawei-Multi/Q34.png)

#### Explanation

**Question:** Based on the spanning tree status of GE0/0/1, which statements are true?
`Designated Bridge/Port : 32768.4c1f-cc4f-26df`
`Port Cost(Dot1T):Config=100`
**A.** Default priority is 32767.
**B.** The switch uses the default priority.
**C.** Administrator changed the path cost using `stp path cost`.
**D.** Path cost calculation is legacy standard.
**Correct Answer: BC**

**Explanation:**

* **Priority (B):** The output shows `32768`, which is the default priority for STP. (A is false because the default is 32768, not 32767).
* **Cost (C):** The `Config=100` indicates a manual setting. Under the default Dot1T (802.1t) standard, a Gigabit port cost is typically 20,000. 100 is a manual override.
* **Standard (D):** The output explicitly says `(Dot1T)`, which is the "Dot1T" standard, not the "Legacy" standard.

---

### Q35.png
![Q35](Huawei-Multi/Q35.png)

#### Explanation

**Question:** Which statements are true about the default preference of common routes?
**A.** Static route is 60.
**B.** Direct route is 0.
**C.** OSPF external route is 255.
**D.** OSPF internal route is 10.
**Correct Answer: ABD**

**Explanation:**

Huawei VRP default Route Preferences:

* **Direct:** 0
* **OSPF Internal:** 10
* **Static:** 60
* **OSPF External (ASE):** **150** (C is false; 255 represents an unreachable or rejected route).

---

### Q36.png
![Q36](Huawei-Multi/Q36.png)

#### Explanation

**Question:** Which statements about IP and MAC addresses are true?
**A.** IP addresses are unchangeable.
**B.** MAC length is 48 bits.
**C.** MAC addresses are unchangeable.
**D.** IP address length is 32 bits.
**Correct Answer: BCD**

**Explanation:**

* **IP (D):** IPv4 is 32 bits. They are **changeable** (A is false) because they are logical addresses assigned based on location.
* **MAC (B, C):** MAC addresses are 48 bits and are burned into the hardware (NIC), making them "unchangeable" physical addresses.

---

### Q37.png
![Q37](Huawei-Multi/Q37.png)

#### Explanation

**Question:** Which statements about OSPF default route advertisement are **false**?
**A.** Preference of advertised default route is 10.
**B.** `default-route-advertise always` works even if no default route exists locally.
**C.** `default-route-advertise` works only if a default route exists locally.
**D.** A router will definitely add an OSPF default route to its table.
**Correct Answer: AD**

**Explanation:**

* **A is False:** The preference of the OSPF route in the table follows the OSPF protocol (10 or 150), but the question implies the "advertised" preference is fixed, which is misleading. More importantly, **D is False** because even if a router learns a default route, it won't add it if a route with a better preference (like a Static route) already exists.

---

### Q38.png
![Q38](Huawei-Multi/Q38.png)

#### Explanation

**Question:** Which comply with the IPv6 abbreviation rules for `2001:0DB8:0000:1234:FB00:0000:5000:45FF`?
**A.** 2001:DB8:0:1234:FB00::5000:45FF
**B.** 2001:DB8:0:1234:FB00::5:45FF
**C.** 2001:0DB8:0:1234:FB00:0:5000:45FF
**D.** 2001:DB8::1234:FB00:0:5000:45FF
**Correct Answer: ACD**

**Explanation:**

* **A & D:** Correctly use `::` to represent one or more blocks of zeros and omit leading zeros.
* **C:** Correctly omits leading zeros in the third and sixth blocks but doesn't use `::`. This is a valid abbreviation.
* **B is False:** It shortens `5000` to `5`. You can only omit **leading** zeros; trailing zeros must remain.

---

### Q39.png
![Q39](Huawei-Multi/Q39.png)

#### Explanation

**Question:** Which of the following are wireless network types based on application scope?
**A.** WPAN (Personal)
**B.** WMAN (Metropolitan)
**C.** WWAN (Wide)
**D.** WLAN (Local)
**Correct Answer: ABCD**

**Explanation:**

Wireless networks are classified by distance:

* **WPAN:** Bluetooth (meters).
* **WLAN:** Wi-Fi (100 meters).
* **WMAN:** WiMAX (kilometers).
* **WWAN:** 4G/5G/Satellite (cities/countries).

---

### Q40.png
![Q40](Huawei-Multi/Q40.png)

#### Explanation

**Question:** Which components are included in the standard NFV architecture?
**A.** NFVI (Infrastructure)
**B.** VNF (Virtual Functions)
**C.** OS
**D.** Mano (Management & Orchestration)
**Correct Answer: ABD**

**Explanation:**

The ETSI NFV standard architecture consists of three main parts:

1. **NFVI (A):** The hardware and virtualization layer.
2. **VNF (B):** The software implementation of network functions.
3. **NFV-MANO (D):** The management and orchestration entity.
While an "OS" (C) runs inside a VNF, it is not a primary component of the architectural framework itself.

---

### Q41.png
![Q41](Huawei-Multi/Q41.png)

---

### Q42.png
![Q42](Huawei-Multi/Q42.png)

---

### Q43.png
![Q43](Huawei-Multi/Q43.png)

---

### Q44.png
![Q44](Huawei-Multi/Q44.png)

---

### Q45.png
![Q45](Huawei-Multi/Q45.png)

---

### Q46.png
![Q46](Huawei-Multi/Q46.png)

---

### Q47.png
![Q47](Huawei-Multi/Q47.png)

---

### Q48.png
![Q48](Huawei-Multi/Q48.png)

---

### Q49.png
![Q49](Huawei-Multi/Q49.png)

---

### Q50.png
![Q50](Huawei-Multi/Q50.png)

**Total Multiple-Choice Questions:** 20

---

## True/False Questions (Q51-Q60)

**Location:** `Huawei-TF/`

### Q51.png
![Q51](Huawei-TF/Q51.png)

#### Explanation

**Question:** Python can run in both interactive mode and non-interactive [script] mode.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Python is highly flexible in its execution:

* **Interactive Mode:** Allows you to type code line-by-line in the Python shell (REPL) and see immediate results. This is great for testing and debugging.
* **Script Mode:** Involves writing code into a file (e.g., `script.py`) and executing the entire file at once. This is the standard for building applications.

---

### Q52.png
![Q52](Huawei-TF/Q52.png)

#### Explanation

**Question:** Switches can implement communication between homogeneous networks or communication between heterogeneous networks and isolate broadcast domains.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

There are two reasons this is "Wrong":

1. **Network Type:** Switches (Layer 2) typically connect **homogeneous** networks (e.g., Ethernet to Ethernet). Connecting **heterogeneous** networks (like Ethernet to Frame Relay or ATM) is a function of a **Router** (Layer 3).
2. **Broadcast Domains:** By default, switches **forward** broadcasts to all ports. Only **Routers** (or VLANs configured on a switch) can isolate or "break" a broadcast domain.

---

### Q53.png
![Q53](Huawei-TF/Q53.png)

#### Explanation

**Question:** In STP, a non-root-bridge switch can have two root ports.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

In the Spanning Tree Protocol (STP), the rules for port selection are strict:

* **Root Bridge:** Has no root ports (all its ports are Designated).
* **Non-Root Bridge:** Must have **exactly one Root Port**. This is the port with the lowest path cost back to the Root Bridge. If multiple paths exist, STP chooses one and blocks the others to prevent loops.

---

### Q54.png
![Q54](Huawei-TF/Q54.png)

#### Explanation

**Question:** In the WLAN network architecture, ACs can be connected in-path or off-path mode.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

An AC (Access Controller) can be deployed in two physical modes:

* **In-path (Direct):** All data traffic from the APs passes through the AC before going to the core network.
* **Off-path (Side-path/Bypass):** The AC only handles the management/control traffic (CAPWAP). The actual user data traffic bypasses the AC and goes directly into the network switches, reducing the AC's workload.

---

### Q55.png
![Q55](Huawei-TF/Q55.png)

#### Explanation

**Question:** SNMP is a standard-based network management protocol... An SNMP NMS and SNMP agent communicate with each other through the TCP protocol.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

SNMP (Simple Network Management Protocol) primarily uses the **UDP** protocol for communication.

* **NMS to Agent:** UDP Port 161 (for queries like Get/Set).
* **Agent to NMS:** UDP Port 162 (for unsolicited Traps/Informs).
While some specific implementations can support TCP for security reasons, the standard and most common deployment is UDP.

---

### Q56.png
![Q56](Huawei-TF/Q56.png)

#### Explanation

**Question:** After receiving a tagged frame from the peer device, an access port of a switch checks the VLAN ID of the frame. If the VLAN ID is the same as PVID of the port, the port accepts the frame.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Access ports are designed for devices that do not understand tags (like PCs). However, if an access port receives a **tagged** frame:

1. It checks the tag's VLAN ID.
2. If the Tag ID matches the port's **PVID** (Port VLAN ID), it accepts the frame, strips the tag, and processes it.
3. If it doesn't match, the frame is discarded.

---

### Q57.png
![Q57](Huawei-TF/Q57.png)

#### Explanation

**Question:** TFTP uses TCP to transfer files, and the default server port number is 21.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

This statement confuses **FTP** and **TFTP**:

* **FTP:** Uses **TCP** and port **21** for control.
* **TFTP (Trivial FTP):** Uses **UDP** and port **69**. It is a much simpler, connectionless protocol with no authentication or directory listing.

---

### Q58.png
![Q58](Huawei-TF/Q58.png)

#### Explanation

**Question:** As every two nodes in a full-mesh network are connected using cables, each node requires a large number of physical ports and connection cables, resulting in relatively high costs.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

In a **Full-Mesh** topology, every device has a direct point-to-point link to every other device.

* For n nodes, the number of links required is n(n-1)/2.
* This provides the highest redundancy and reliability, but the cabling and port requirements grow exponentially, making it extremely expensive and difficult to scale.

---

### Q59.png
![Q59](Huawei-TF/Q59.png)

#### Explanation

**Question:** WLAN technology enables transmission of information by radio waves over the air. Currently, the 2.6 GHz and 5 GHz frequency bands are used.
**A.** Right
**B.** Wrong
**Correct Answer: Wrong**

**Explanation:**

The standard unlicensed frequency bands for Wi-Fi are **2.4 GHz** and **5 GHz**.

* **2.6 GHz** is typically a licensed band used for mobile cellular networks (like LTE/4G), not standard WLAN/Wi-Fi.

---

### Q60.png
![Q60](Huawei-TF/Q60.png)

#### Explanation

**Question:** Segment routing (SR) can be deployed with or without controllers.
**A.** Right
**B.** Wrong
**Correct Answer: Right**

**Explanation:**

Segment Routing is highly adaptable:

* **Without a Controller:** Routers use a distributed control plane (like OSPF or IS-IS with SR extensions) to calculate paths independently.
* **With a Controller:** A centralized SDN controller (like a PCE) can be used to manage traffic engineering and complex path calculations across the whole network.

**Total True/False Questions:** 10

---

## Summary Statistics

| Question Type | Count | Question Numbers | Location |
|---------------|-------|------------------|----------|
| Single-Choice | 30 | Q1-Q30 | `Huawei-Single/` |
| Multiple-Choice | 20 | Q31-Q50 | `Huawei-Multi/` |
| True/False | 10 | Q51-Q60 | `Huawei-TF/` |
| **TOTAL** | **60** | **Q1-Q60** | |

---

## Usage

1. Scroll through this README to view all mock exam questions as images
2. Use these questions to practice for the HCIA-Datacom certification exam
3. Test your knowledge across all topics covered in the certification
4. Review the questions and compare with the chapter quizzes in `CHAPTER_QUIZZES_README.md`
5. Use these as a comprehensive practice exam before taking the actual certification test

---

## Related Documentation

- **Chapter Quizzes**: See `CHAPTER_QUIZZES_README.md` for chapter-specific quiz questions with explanations
- **Chapter Answers**: See `Chapter_Answers.md` for comprehensive answers to all chapter questions
- **Main Study Guide**: See `Huawei_HCIA-Datacom.md` for the complete study guide with all topics

---

## Exam Tips

- **Single-Choice Questions**: Read all options carefully before selecting your answer. Eliminate obviously wrong answers first.
- **Multiple-Choice Questions**: Select ALL correct answers. Partial credit is typically not given.
- **True/False Questions**: Pay attention to absolute terms like "always," "never," "all," or "none" as these often indicate false statements.
- **Time Management**: Practice with these questions to improve your speed and accuracy.
- **Review**: After completing the mock exam, review any questions you were unsure about using the chapter study materials.

---

*Last updated: 2024*
