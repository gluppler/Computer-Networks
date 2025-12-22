
---

### **Q31**

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

### **Q32**

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

### **Q33**

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

### **Q34**

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

### **Q35**

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

### **Q36**

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

### **Q37**

**Question:** Which statements about OSPF default route advertisement are **false**?
**A.** Preference of advertised default route is 10.
**B.** `default-route-advertise always` works even if no default route exists locally.
**C.** `default-route-advertise` works only if a default route exists locally.
**D.** A router will definitely add an OSPF default route to its table.
**Correct Answer: AD**

**Explanation:**

* **A is False:** The preference of the OSPF route in the table follows the OSPF protocol (10 or 150), but the question implies the "advertised" preference is fixed, which is misleading. More importantly, **D is False** because even if a router learns a default route, it won't add it if a route with a better preference (like a Static route) already exists.

---

### **Q38**

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

### **Q39**

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

### **Q40**

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

